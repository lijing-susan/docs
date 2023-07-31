---
title: 数据集管理
---

## 查看全部数据集

点击左侧**数据集**菜单栏即可查看所属该项目的全部数据集，数据集列表展示了数据集的基本信息，包括：数据集名称、最新版本别名、数据集归属人和数据集创建时间等。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/list.png)

## 查看数据集详情

数据集详情包含3个部分，概览，元数据和数据文件

**概览**

概览展示了数据集版本的基本信息，包括：数据集名称，数据集版本名称，数据集版本别名，数据集版本是否共享和数据集版本创建时间。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/detail.png)

:::caution
属于公开项目的数据集可以被共享，任何人可见和可以使用共享数据集。了解更多操作权限问题，详见[角色和权限](https://doc.starwhale.ai/docs/concepts/roles-permissions) 
:::

**元数据**

数据集的元数据，包括数据集构建信息，构建数据集使用的Starwhale版本和数据集的概要信息。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/meta.png)

**数据文件**

支持可视化展示数据和标注，支持的数据格式详见

| 数据类型 | 格式 | 标注类型 |
|---|---|---|
| 图片 |jpg, jpeg, png | 2D Box, 2D Polygon, 2D Polyline, 2D Keypoint, Classification, Segmentation |
| 视频 | MP4 | Classification |
| 音频 | MP3, wav | Classification |
| 文本 | txt | Classification |

## 数据集可视化展示

### 图片查看

支持图表或者大图模式查看图片数据

**图表模式**

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/inmage%20viewer.png)

**大图模式**

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/image%20viewer%20full.png)
  
大图左侧显示标注信息和元数据

勾选 Bounding box 复选框，展示 bounding box名称；取消勾选，则不显示bounding box

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/annotation.png)

可以通过点击**眼睛**按钮，来控制全部显示、全部不显示或者部分显示bounding box

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/not%20display.png)

### 视频查看

支持图表或者大图模式查看视频数据

**图表模式**

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/video.jpg)

**大图模式**

左侧显示标注信息

右下角有操作按钮，支持播放/暂停，调节音量，调整播放速度和全屏操作

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/videofull.jpg)

### 音频查看

支持图表或者大图模式查看音频数据

**图表模式**

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/audio.png)

**大图模式**

1 左侧显示标注信息

2 右下角有操作按钮，支持播放/暂停，调节音量操作。点击**更多**，可以下载和调整播放速度。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/audio%20full.png)

### 文本数据

支持图标或者大图模式查看文本数据

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/text.png)

## 数据集共享

进入详情**概览**页，打开共享开关，可共享数据集；关闭共享开关，即可停止共享。属于公开项目的数据集可以被共享，共享后对所有用户可见和可使用。了解更多操作权限问题，详见[角色和权限](https://doc.starwhale.ai/docs/concepts/roles-permissions) 

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/share.png)

## 移除数据集

点击**移除**按钮，然后点击**是**确认，点击**否**取消。

:::caution
如果确认移除的话，数据集的所有版本都会被移除.
:::

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/remove.png)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/confirm.png)

## 恢复指定版本数据集

进入**回收站**，找到要恢复的数据集，点击**还原**按钮，然后点击**是**确认即可恢复数据集。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/restore.png)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/restore%20confirm.png)

## 删除数据集

进入**回收站**模块，找到需要删除的数据集，点击**删除**，然后点击**是**确认即可彻底删除数据集。

:::danger
如果确认删除数据集，数据集将无法再被恢复
:::

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/delete.jpg)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/manage/delete%20confirm.jpg)
