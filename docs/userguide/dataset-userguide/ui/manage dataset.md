---
title: Manage a Starwhale Dataset by UI
---

## Starwhale Dataset list {#list}

Starwhale dataset list displays the basic dataset information: Dataset name, the latest dataset version alias, dataset owner, the created time and dataset actions.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/list.png)

## Starwhale Dataset Detail Information {#info}

Dataset version information consists of overview, metadata, and files.

**Overview** 

The basic information of a dataset version, including dataset name, dataset version name, dataset version aliases, whether the dataset version is shared, and the created time of a dataset version.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/detail.png)

:::caution
Switch the button to set a dataset version to a shared mode if the dataset belongs to a public project. A shared dataset can be seen and used for everyone. For more information, see [Roles and permissions](https://doc.starwhale.ai/docs/concepts/roles-permissions) 
:::

**Metadata**

The metadata of the dataset, including the building os information, Starwhale version information, and dataset summarized information.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/meta.png)

**Files**

We are supporting viewing data like videos, images, audio, texts, and annotations.

| Data Types | Format | Annotation Types |
|---|---|---|
| Images |jpg, jpeg, png | 2D Box, 2D Polygon, 2D Polyline, 2D Keypoint, Classification, Segmentation |
| Videos | MP4 | Classification |
| Audios | MP3, wav | Classification |
| Texts | txt | Classification |

## Starwhale Dataset Visualization {#visualize}

### Image data viewer

Image data visualization support viewing image data in tables(default) or a larger view.

- **Table view**

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/inmage%20viewer.png)

- **Full view**

  The left side of the full view displays the annotation information supporting choosing whether the annotations should be displayed.

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/image%20viewer%20full.png)

### Video data viewer**
  
- **Table view**

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/video.jpg)

- **Full view**

  Video data visualization support viewing audio data in tables(default) or a larger view.

  1 The left side of the full view displays the annotation information.

  2 The lower right corner can play/pause, play volume, play speed and play in full screen.

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/videofull.jpg)

### Audio data viewer
 
Audio data visualization support viewing audio data in tables(default) or a complete view.

- **Table view**

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/audio.png)

- **Full view**

  1 The left side of the full view displays the annotation information

  2 The lower right corner can play/pause and play volume. Click More, can download and adjust the play speed.

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/audio%20full.png)

### Text data viewer

Text data visualization support viewing text data in tables(default) or a full view

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/text.png)

## Share a Starwhale Dataset {#share}

Easily switch between shared and unshared modes for dataset versions by clicking the designated button. If the dataset is part of a public project. For more information, see [Roles and permissions users can access and utilise a shared dataset ifissions](https://dopc.starwhale.ai/docs/concepts/roles-permissions)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/share.png)

## Remove a Starwhale Dataset {#remove}

Click **Remove** first, then click **Yes** to confirm or click **No** to cancel.

:::caution
If you confirm to remove, all dataset versions will be removed.
:::

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/remove.png)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/confirm.png)

## Recover a preciously removed Starwhale Dataset {#recover}

You can go to **Trash** to find the dataset you want to recover, then click **Restore** to recover your datasets. And then, click **Yes** to confirm or click **No** to cancel.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/restore.png)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/restore%20confirm.png)

## Delete a dataset

You can go to **Trash**, search for the dataset you want to delete, then click **Delete** to delete a dataset, and then click **Yes** to confirm or **No** to cancel. 

:::danger
If you confirm to delete, all versions of a dataset will be deleted and will not be recovered any more.
:::

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/delete.jpg)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/delete%20confirm.jpg)
