---
title: Starwhale 数据类型 SDK
---

## COCOObjectAnnotation

提供COCO类型的定义。

```python
COCOObjectAnnotation(
    id: int,
    image_id: int,
    category_id: int,
    segmentation: Union[t.List, t.Dict],
    area: Union[float, int],
    bbox: Union[BoundingBox, t.List[float]],
    iscrowd: int,
)
```

|参数|说明|
|---|---|
|`id`|object id，一般为全局object的递增id|
|`image_id`|image id，一般为图片id|
|`category_id`|category id，一般为目标检测中类别的id|
|`segmentation`|物体轮廓表示，Polygon(多边形的点)或RLE格式|
|`area`|object面积|
|`bbox`|表示bounding box，可以为BoundingBox类型或float的列表|
|`iscrowd`|0表示是一个单独的object，1表示两个没有分开的object|

### 使用示例 {#coco-example}

```python
def _make_coco_annotations(
    self, mask_fpath: Path, image_id: int
) -> t.List[COCOObjectAnnotation]:
    mask_img = PILImage.open(str(mask_fpath))

    mask = np.array(mask_img)
    object_ids = np.unique(mask)[1:]
    binary_mask = mask == object_ids[:, None, None]
    # TODO: tune permute without pytorch
    binary_mask_tensor = torch.as_tensor(binary_mask, dtype=torch.uint8)
    binary_mask_tensor = (
        binary_mask_tensor.permute(0, 2, 1).contiguous().permute(0, 2, 1)
    )

    coco_annotations = []
    for i in range(0, len(object_ids)):
        _pos = np.where(binary_mask[i])
        _xmin, _ymin = float(np.min(_pos[1])), float(np.min(_pos[0]))
        _xmax, _ymax = float(np.max(_pos[1])), float(np.max(_pos[0]))
        _bbox = BoundingBox(
            x=_xmin, y=_ymin, width=_xmax - _xmin, height=_ymax - _ymin
        )

        rle: t.Dict = coco_mask.encode(binary_mask_tensor[i].numpy())  # type: ignore
        rle["counts"] = rle["counts"].decode("utf-8")

        coco_annotations.append(
            COCOObjectAnnotation(
                id=self.object_id,
                image_id=image_id,
                category_id=1,  # PennFudan Dataset only has one class-PASPersonStanding
                segmentation=rle,
                area=_bbox.width * _bbox.height,
                bbox=_bbox,
                iscrowd=0,  # suppose all instances are not crowd
            )
        )
        self.object_id += 1

    return coco_annotations
```

## GrayscaleImage

提供灰度图类型，比如MNIST中数字手写体图片，是 `Image` 类型的一个特例。

```python
GrayscaleImage(
    fp: _TArtifactFP = "",
    display_name: str = "",
    shape: Optional[_TShape] = None,
    as_mask: bool = False,
    mask_uri: str = "",
)
```

|参数|说明|
|---|---|
|`fp`|图片的路径、IO对象或文件内容的bytes|
|`display_name`|Dataset Viewer上展示的名字|
|`shape`|图片的Width和Height，channel默认为1|
|`as_mask`|是否作为Mask图片|
|`mask_uri`|Mask原图的URI|

### 使用示例 {#gray-example}

```python
for i in range(0, min(data_number, label_number)):
    _data = data_file.read(image_size)
    _label = struct.unpack(">B", label_file.read(1))[0]
    yield GrayscaleImage(
        _data,
        display_name=f"{i}",
        shape=(height, width, 1),
    ), {"label": _label}
```

### GrayscaleImage函数

#### GrayscaleImage.to_types

```python
to_bytes(encoding: str= "utf-8") -> bytes
```

#### GrayscaleImage.carry_raw_data

```python
carry_raw_data() -> GrayscaleImage
```

#### GrayscaleImage.astype

```python
astype() -> Dict[str, t.Any]
```

## BoundingBox

提供边界框类型，目前为 `LTWH` 格式，即 `left_x`, `top_y`, `width` 和 `height`。

```python
BoundingBox(
    x: float,
    y: float,
    width: float,
    height: float
)
```

|参数|说明|
|---|---|
|`x`|left_x的坐标|
|`y`|top_y的坐标|
|`width`|图片的宽度|
|`height`|图片的高度|

## ClassLabel

描述label的数量和类型。

```python
ClassLabel(
     names: List[Union[int, float, str]]
)
```

## Image

图片类型。

```python
Image(
    fp: _TArtifactFP = "",
    display_name: str = "",
    shape: Optional[_TShape] = None,
    mime_type: Optional[MIMEType] = None,
    as_mask: bool = False,
    mask_uri: str = "",
)
```

|参数|说明|
|---|---|
|`fp`|图片的路径、IO对象或文件内容的bytes|
|`display_name`|Dataset Viewer上展示的名字|
|`shape`|图片的Width、Height和channel|
|`mime_type`|MIMEType支持的类型|
|`as_mask`|是否作为Mask图片|
|`mask_uri`|Mask原图的URI|

### 使用示例 {#image-example}

```python
import io
import typing as t
import pickle
from PIL import Image as PILImage
from starwhale import Image, MIMEType

def _iter_item(paths: t.List[Path]) -> t.Generator[t.Tuple[t.Any, t.Dict], None, None]:
    for path in paths:
        with path.open("rb") as f:
            content = pickle.load(f, encoding="bytes")
            for data, label, filename in zip(
                content[b"data"], content[b"labels"], content[b"filenames"]
            ):
                annotations = {
                    "label": label,
                    "label_display_name": dataset_meta["label_names"][label],
                }

                image_array = data.reshape(3, 32, 32).transpose(1, 2, 0)
                image_bytes = io.BytesIO()
                PILImage.fromarray(image_array).save(image_bytes, format="PNG")

                yield Image(
                    fp=image_bytes.getvalue(),
                    display_name=filename.decode(),
                    shape=image_array.shape,
                    mime_type=MIMEType.PNG,
                ), annotations
```

### Image函数

#### Image.to_types

```python
to_bytes(encoding: str= "utf-8") -> bytes
```

#### Image.carry_raw_data

```python
carry_raw_data() -> GrayscaleImage
```

#### Image.astype

```python
astype() -> Dict[str, t.Any]
```

## Video

视频类型。

```python
Video(
    fp: _TArtifactFP = "",
    display_name: str = "",
    mime_type: Optional[MIMEType] = None,
)
```

|参数|说明|
|---|---|
|`fp`|视频的路径、IO对象或文件内容的bytes|
|`display_name`|Dataset Viewer上展示的名字|
|`mime_type`|MIMEType支持的类型|

### 使用示例 {#video-example}

```python
import typing as t
from pathlib import Path

from starwhale import Video, MIMEType

root_dir = Path(__file__).parent.parent
dataset_dir = root_dir / "data" / "UCF-101"
test_ds_path = [root_dir / "data" / "test_list.txt"]

def iter_ucf_item() -> t.Generator:
    for path in test_ds_path:
        with path.open() as f:
            for line in f.readlines():
                _, label, video_sub_path = line.split()

                data_path = dataset_dir / video_sub_path
                data = Video(
                    data_path,
                    display_name=video_sub_path,
                    shape=(1,),
                    mime_type=MIMEType.WEBM,
                )

                yield f"{label}_{video_sub_path}", {
                    "video": data,
                    "label": label,
                }
```

## Audio

音频类型。

```python
Audio(
    fp: _TArtifactFP = "",
    display_name: str = "",
    mime_type: Optional[MIMEType] = None,
)
```

|参数|说明|
|---|---|
|`fp`|音频文件的路径、IO对象或文件内容的bytes|
|`display_name`|Dataset Viewer上展示的名字|
|`mime_type`|MIMEType支持的类型|

### 使用示例 {#audio-example}

```python
import typing as t
from starwhale import Audio

def iter_item() -> t.Generator[t.Tuple[t.Any, t.Any], None, None]:
    for path in validation_ds_paths:
        with path.open() as f:
            for item in f.readlines():
                item = item.strip()
                if not item:
                    continue

                data_path = dataset_dir / item
                data = Audio(
                    data_path, display_name=item, shape=(1,), mime_type=MIMEType.WAV
                )

                speaker_id, utterance_num = data_path.stem.split("_nohash_")
                annotations = {
                    "label": data_path.parent.name,
                    "speaker_id": speaker_id,
                    "utterance_num": int(utterance_num),
                }
                yield data, annotations
```

### Audio函数

#### Audio.to_types

```python
to_bytes(encoding: str= "utf-8") -> bytes
```

#### Audio.carry_raw_data

```python
carry_raw_data() -> Audio
```

#### Audio.astype

```python
astype() -> Dict[str, t.Any]
```

## Text

文本类型，默认为 `utf-8` 格式。

```python
Text(
    content: str,
    encoding: str = "utf-8",
)
```

|参数|说明|
|---|---|
|`content`|text内容|
|`encoding`|text的编码格式|

### 使用示例 {#text-example}

```python
import typing as t
from pathlib import Path
from starwhale import Text

def iter_item(self) -> t.Generator[t.Tuple[t.Any, t.Any], None, None]:
    root_dir = Path(__file__).parent.parent / "data"

    with (root_dir / "fra-test.txt").open("r") as f:
        for line in f.readlines():
            line = line.strip()
            if not line or line.startswith("CC-BY"):
                continue

            _data, _label, *_ = line.split("\t")
            data = Text(_data, encoding="utf-8")
            annotations = {"label": _label}
            yield data, annotations
```

### Text函数

#### to_types

```python
to_bytes(encoding: str= "utf-8") -> bytes
```

#### Text.carry_raw_data

```python
carry_raw_data() -> Text
```

#### Text.astype

```python
astype() -> Dict[str, t.Any]
```

#### Text.to_str

```python
to_str() -> str
```

## Binary

二进制类型，用bytes存储。

```python
Binary(
    fp: _TArtifactFP = "",
    mime_type: MIMEType = MIMEType.UNDEFINED,
)
```

|参数|说明|
|---|---|
|`fp`|路径、IO对象或文件内容的bytes|
|`mime_type`|MIMEType支持的类型|

### Binary函数

#### Binary.to_types

```python
to_bytes(encoding: str= "utf-8") -> bytes
```

#### Binary.carry_raw_data

```python
carry_raw_data() -> Binary
```

#### Binary.astype

```python
astype() -> Dict[str, t.Any]
```

## Link

Link类型，用来制作 `remote-link` 类型的数据集。

```python
Link(
    uri: str,
    auth: Optional[LinkAuth] = DefaultS3LinkAuth,
    offset: int = 0,
    size: int = -1,
    data_type: Optional[BaseArtifact] = None,
)
```

|参数|说明|
|---|---|
|`uri`|原始数据的uri地址，目前支持localFS和S3两种协议|
|`auth`|Link Auth信息|
|`offset`|数据相对uri指向的文件偏移量|
|`size`|数据大小|
|`data_type`|Link指向的实际数据类型，目前支持 `Binary`, `Image`, `Text`, `Audio` 和 `Video` 类型|

### Link函数

#### Link.astype

```python
astype() -> Dict[str, t.Any]
```

## MIMEType

描述Starwhale支持的多媒体类型，用Python Enum类型实现，用在 `Image`、`Video` 等类型的mime_type 属性上，能更好的进行Dataset Viewer。

```python
class MIMEType(Enum):
    PNG = "image/png"
    JPEG = "image/jpeg"
    WEBP = "image/webp"
    SVG = "image/svg+xml"
    GIF = "image/gif"
    APNG = "image/apng"
    AVIF = "image/avif"
    PPM = "image/x-portable-pixmap"
    MP4 = "video/mp4"
    AVI = "video/avi"
    WEBM = "video/webm"
    WAV = "audio/wav"
    MP3 = "audio/mp3"
    PLAIN = "text/plain"
    CSV = "text/csv"
    HTML = "text/html"
    GRAYSCALE = "x/grayscale"
    UNDEFINED = "x/undefined"
```

## Line

描述直线。

```python
from starwhale import ds, Point, Line

with dataset("collections") as ds:
    line_points = [
        Point(x=0.0, y=1.0),
        Point(x=0.0, y=100.0)
    ]
    ds.append({"line": line_points})
    ds.commit()
```

## Point

描述点。

```python
from starwhale import ds, Point

with dataset("collections") as ds:
    ds.append(Point(x=0.0, y=100.0))
    ds.commit()
```

## Polygon

描述多边形。

```python
from starwhale import ds, Point, Polygon

with dataset("collections") as ds:
    polygon_points = [
        Point(x=0.0, y=1.0),
        Point(x=0.0, y=100.0),
        Point(x=2.0, y=1.0),
        Point(x=2.0, y=100.0),
    ]
    ds.append({"polygon": polygon_points})
    ds.commit()
```
