---
title:报告管理
---
Starwhale的报告是一个富文本编辑器，支持您将模型评测的结果以文档的形式呈现出来，同时可以将报告进行分享

## 报告查看

### 查看报告列表

点击左侧导航栏 **报告** 图标，即可进入报告列表页查看该项目下的

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/list.jpg)

### 查看报告详情

点击 **报告标题** 或者 操作列 **预览**，即可查看报告详情。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/view.jpg)

## 报告创建

点击报告列表页右上角 **创建** 按钮，即可新建报告

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/create%20button.jpg)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/create%20report.jpg)

## 编辑与编排

在报告中，我们使用“块”去称呼结构化元素。报告里的每一种内容类型都是一种“块”，包括文本段落、标题、面板等。

在报告中可以插入“块”，一边编辑和编排出一篇您满意的报告。

在报告任意空白行输入** /** ，或正文任意位置输入**空格 /** 即可触发 **快速插入**，显示工具栏菜单，然后插入“块”。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/toolbar.jpg)

### 拆入文本

在报告任意空白行输入 **/** ，或正文任意位置输入空格 / 即可触发 **快速插入**，在工具栏中选择 **文本** 即可

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/text.jpg)

### 插入目录

**插入目录**

在报告任意空白行输入 **/** ，或正文任意位置输入 **空格 /** 即可触发 **快速插入**，在工具栏中菜单中选择 **标题级别** 即可

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/heading.jpg)

**转换为目录**

将鼠标悬浮在一段文字上，在报告左侧的 T⋮⋮ 工具栏中选择 **标题级别**，即可将这段文字转换为标题

### 有序列表和无序列表

在报告任意空白行输入 / ，或正文任意位置输入 **空格 /** 即可触发 **快速插入**，在工具栏中选择 **有序列表** 或 **无序列表** 即可

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/number%20and%20bullet%20list.jpg)

### 插入代码块

**插入代码块**

在报告任意空白行输入 **/** ，或正文任意位置输入 **空格 /** 即可触发 **快速插入**，在工具栏中选择 **代码块** 即可

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/code.jpg)

**转换为代码块**

将鼠标悬浮在一段文字上，在报告左侧的 T⋮⋮ 工具栏中选择 **代码块**，即可将这段文字转换为代码块展示

**切换代码语言**

在代码块的左上角，点击可查看、搜索和切换编辑语言。切换后代码块左上角将显示目前选择的编程语言

### 在报告中使用引用

在报告任意空白行输入 **/** ，或正文任意位置输入**空格 /** 即可触发 **快速插入**，在工具栏中选择 **引用** 即可

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/quote.jpg)

### 插入面板

**1.编辑面板**

- 插入面板

在报告任意空白行输入 **/** ，或正文任意位置输入 **空格 /** 即可触发 **快速插入**，在工具栏中选择 **面板** 即可

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/panel.jpg)

- 重命名面板

点击 **设置** > **重命名**，输入名称

【截图】

- 删除面板

点击 **删除**，点击确认弹窗中 **是的** 按钮， 即可将选中的面板删除

【截图】
  
**2.添加数据**

- 添加评测数据

点击右侧 **添加评测** 按钮，勾选想展示的评测数据，点击 **添加**。支持跨项目选择评测数据，可在选择项目菜单切换项目。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/add_eval.jpg)

- 移除评测数据

点击 **移除** 按钮，即可将已选评测数据移除。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/remove.jpg)

- 字段设置

点击 **设置**，可设置面板评测列表里的展示的字段，可见字段为展示在评测列表里的字段。

【截图】

**3.添加图表**

- 添加图表

如想将数据以图表的方式展现，点击右侧 **添加图表** 按钮，选择图表类型，数据表，X轴和Y轴展示的数据，图表名称，点击 **提交**。

注：表格和图表存在联动关系，通过表格选取的数据范围就是图表可以选择的最大数据范围。

【截图】

- 编辑图表大小

鼠标hover在图表右下角，通过拖拽可编辑图表大小

【截图】

- 编辑图表

点击 **设置** > **编辑图表**，即可对图表类型、数据表、图表名称等进行编辑，点击 **提交** 保存编辑内容

- 删除图表

点击 **设置** > **删除**，点击确认弹窗里的 **是的** 按钮，即可将图表删除

## 分享及权限

点击 **分享**开关，可将报告

【截图】

## 移除报告

在报告列表页，点击 **移除** 按钮可将报告移除至回收站。了解更多操作权限详情，请参考[Starwhale的角色和权限](https://starwhale.cn/docs/concepts/roles-permissions)

【截图】

## 恢复报告

点击左侧导航栏 **回收站** 图表，进入回收站列表，点击 **恢复**即可。了解更多操作权详情，请参考[Starwhale的角色和权限](https://starwhale.cn/docs/concepts/roles-permissions)

【截图】
