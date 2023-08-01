---
title: 模型评测
---

## 创建评测

1 点击列表页右上角 “**创建**” 按钮；

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/create%201.jpg)

2 选择和填写创建页表单:

  - 选择 **资源池**，不同资源池代表不同的计算资源；
  - 选择 **模型版本** 和 handler；
  - 选择 **数据集版本**；
  - 选择 **运行时版本**；
  - 调试模式: 调试模式默认关闭。如您开启调试模式，请记住调试密码以便后续调试时使用；
  - 自动释放: 默认自动释放时间为 3,600 秒; 支持修改为其他时长。如设置自动释放时长，系统到达释放时长时会自动释放资源，取消评测；如不设置自动释放时，除非手动取消，否则系统会一直运行评测直到账户可用余额为0。
    
3 确认资源价格，点击 “**提交**”  创建评测.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/create.png)

## 查看评测列表

评测列表可以查看项目中的所有评测，通过UI、CLI和SDK运行的评测会按照时间顺序由新到旧显示在评测列表页。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/eval%20list.jpg)

### 评测对比

1 勾选想需要进行比较的评测前的复选框，即可进入评测对比模式，支持同时对多个评测进行比较。如需退出评测模式，取消勾选即可；
  
![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/compare.jpg)

2 被固定的评测是基准评测，如果想更换基准评测，请固定其他评测；

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/pin.jpg)

3 点击右下角按钮，可以对评测详情进行对比；

- **评测详情半屏显示** 

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/half-screen.jpg)

- **评测详情全屏显示** 

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/compare-detail-result-full%20screen.jpg)

4 点击“**设置**”按钮可对列字段进行设置。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/collumn.jpg)

- 勾选不需要展示的列字段，然后点击下图标识**①**处的按钮；
- 点击下图标识 **②** 处的按钮，通过拖拽调整列字段显示顺序；
- 点击下图表示 **③** 处的按钮，来固定列字段。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/collumn-1.jpg)
  
## 查看评测详情

### 查看评测结果

点击 **sys/id** 即可查看汇总结果和详细结果。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/sysid.jpg)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/eval-result.jpg)

### 查看评测任务和日志
  
**查看评测任务**

点击评测任务标签页，即可查看该评测的所有评测任务。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/tasks.jpg)

**查看日志**

点击 “**查看日志**” 按钮可查看日志。

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/viewlog.jpg)
