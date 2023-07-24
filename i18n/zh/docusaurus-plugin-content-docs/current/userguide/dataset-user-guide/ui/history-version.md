---
title:数据集版本管理
---

Starwhale数据集版本管理可以协助您对数据集的版本进行管理，支持历史版本的查看、共享和云端一键下载到本地

## 数据集历史版本查看

1 在数据集列表页，点击**历史版本**按钮可查看该数据集的全部历史版本。


![image](https://user-images.githubusercontent.com/101299635/234795306-7311c641-ca31-44ae-9c59-a3a66433285a.png)

2 数据集版本列表页展示了数据集版本的基本信息，包含：版本名称、版本别名，版本是否共享和版本的创建时间等。

![image](https://user-images.githubusercontent.com/101299635/234825710-37a13e18-7df1-471c-b339-445f49435c91.png)

:::catution
如果您共享了数据集的某个版本，该数据集版本对所有人可见。如果尚未共享，则只对有权限的用户可见。
:::

## 共享数据集版本

1 您需要在在数据集详情**概览**页面进行操作

2 点击**共享开关**，开关打开则数据集版本处于共享状态，开关关闭则数据集版本处于非共享状态。

:::catution
如果您共享了数据集的某个版本，该数据集版本对所有人可见。如果尚未共享，则只对有权限的用户可见。
:::

![image](https://user-images.githubusercontent.com/101299635/234837932-18a7270f-a1c5-48f6-8aec-5f58458d357c.png)

如果您想共享数据集的所有版本，需要您单独对每个版本进行共享操作。

## 下载指定数据集版本到本地

1 在CLI输入命令 `sw assistance wait-console` 

![image](https://github.com/lijing-susan/docs/assets/101299635/63364c6c-92c7-4f1d-bd1d-216a19acb228)

2 点击**下载到本地**按钮就能将数据集指定版本下载到本地了。

![image](https://github.com/lijing-susan/docs/assets/101299635/0fb349ee-e275-4f20-98a8-d6924320c47b)
