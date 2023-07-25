---
title:数据集管理
---

## 查看全部数据集

点击左侧**数据集**菜单栏即可查看所属该项目的全部数据集，数据集列表展示了数据集的基本信息，包括：数据集名称、最新版本别名、数据集归属人和数据集创建时间等。

![image](https://user-images.githubusercontent.com/101299635/234795143-2987043e-9dd2-4b73-8ff9-73b83762356e.png)

## 查看数据集详情

数据集详情包含3个部分，概览，元数据和数据文件

**概览**

概览展示了数据集版本的基本信息，包括：数据集名称，数据集版本名称，数据集版本别名，数据集版本是否共享和数据集版本创建时间。

![image](https://user-images.githubusercontent.com/101299635/234795667-e2331a52-351d-4dcd-a5ad-631596cd2ea9.png)

:::caution
属于公开项目的数据集可以被共享，任何人可见和可以使用共享数据集。了解更多操作权限问题，详见[角色和权限](https://doc.starwhale.ai/docs/concepts/roles-permissions) 
:::

**元数据**

数据集的元数据，包括数据集构建信息，构建数据集使用的Starwhale版本和数据集的概要信息。

![image](https://user-images.githubusercontent.com/101299635/234795955-337bd013-782b-48fd-97dc-1af9067ffc1a.png)

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

![image](https://user-images.githubusercontent.com/101299635/234798959-ba214fb9-bf94-413b-b6b5-81d0d9f5ba40.png)

**大图模式**

![image](https://user-images.githubusercontent.com/101299635/234799661-9b33cf77-975f-40be-8f87-55a705848660.png)

大图左侧显示标注信息和元数据

勾选 Bounding box 复选框，展示 bounding box名称；取消勾选，则不显示bounding box

![image](https://github.com/lijing-susan/docs/assets/101299635/4abe9a7a-0e54-4dca-bd01-67ba0fbdd511)

可以通过点击**眼睛**按钮，来控制全部显示、全部不显示或者部分显示bounding box

![image](https://github.com/lijing-susan/docs/assets/101299635/d0d526fb-2bd3-48cb-8ab4-185135aee42b)

### 视频查看

支持图表或者大图模式查看视频数据

**图表模式**

 ![img_v2_9a04dddd-6c39-4b45-8763-075798f1e48g](https://user-images.githubusercontent.com/101299635/234829713-42ca7580-d2b6-4e98-b9d4-92f8c0e2585d.jpg)

**大图模式**

左侧显示标注信息

右下角有操作按钮，支持播放/暂停，调节音量，调整播放速度和全屏操作

![img_v2_3e961d3c-4d57-42ff-b18a-1d9cf65db64g](https://user-images.githubusercontent.com/101299635/234829798-ea4f6cb2-3c88-43dd-88d9-55e43db3a95c.jpg)

### 音频查看

支持图表或者大图模式查看音频数据

**图表模式**

![image](https://user-images.githubusercontent.com/101299635/234803932-59089931-00c3-4d12-b101-5d4f11191df3.png)

**大图模式**

1 左侧显示标注信息

2 右下角有操作按钮，支持播放/暂停，调节音量操作。点击**更多**，可以下载和调整播放速度。

![image](https://user-images.githubusercontent.com/101299635/234804126-3f6f76b0-95ba-4bf4-9150-6ee7c9563c54.png)

### 文本数据

支持图标或者大图模式查看文本数据

![image](https://user-images.githubusercontent.com/101299635/234797034-84f2c866-a06a-4552-a292-966d9e8522d5.png)

## 数据集共享

进入详情**概览**页，打开共享开关，可共享数据集；关闭共享开关，即可停止共享。属于公开项目的数据集可以被共享，共享后对所有用户可见和可使用。了解更多操作权限问题，详见[角色和权限](https://doc.starwhale.ai/docs/concepts/roles-permissions) 

![image](https://user-images.githubusercontent.com/101299635/234837932-18a7270f-a1c5-48f6-8aec-5f58458d357c.png)

## 移除数据集

点击**移除**按钮，然后点击**是**确认，点击**否**取消。

:::caution
如果确认移除的话，数据集的所有版本都会被移除.
:::

![image](https://github.com/lijing-susan/docs/assets/101299635/8cba965d-d634-4120-9c9a-e2a434503678)

![image](https://github.com/lijing-susan/docs/assets/101299635/eb306408-e0e1-4a76-8bde-37dc49e9b0ff)

## 恢复指定版本数据集

进入**回收站**，找到要恢复的数据集，点击**还原**按钮，然后点击**是**确认，点击**否**取消。

![image](https://github.com/lijing-susan/docs/assets/101299635/d1640061-3ffb-472b-9fd8-a6d7601cb52a)

![image](https://github.com/lijing-susan/docs/assets/101299635/38a0d54e-3c1d-4781-9278-290a6018a21a)
