---
title: Run a Starwhale Model Evaluation by UI
---

## Create a model evaluation

1 Click **Create** to start configuring a model evaluation；

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/create%201.jpg)

2 Select the items on the page:

  - Choose the **resource pool** which contains kinds of compute resources
  - Choose the **model version** and handler
  - Choose the **dataset version**
  - Choose the **runtime version**
  - Debug mode: The debug mode is off on default. If you switch it on, remember the debug password for later debugging.
  - Auto release: The default auto-release time is 3600 seconds; you can change it if needed. If you set the release time, the job will release automatically when the time is up. If you switch off the auto-release, the job will continue until you cancel it.
    
3 Check the price, then Click **Submit** to create an evaluation.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/create.png)

## Model Evaluation List

In the evaluation table, you can see all  the evaluations of one project in one place.

Each time you run an evaluation with Starwhale Web UI, Starwhale Client or Python SDK, it's added to the top of the table.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/eval%20list.jpg)

### Side-by-Side Comparison of Evaluations

1 Select evaluations to compare the summary results by ticking the checkbox to include or exclude evaluations. If you want to exit the compare mode, untick the evaluations you ticked.
  
![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/compare.jpg)

2 The pined evaluation is the base evaluation. If you want to change the base evaluation, pin another evaluation.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/pin.jpg)

3 To compare the result details, click the icon button on the bottom right corner.

- **Result details in half screen** 

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/half-screen.jpg)

- **Result details in full screen** 

  ![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/compare-detail-result-full%20screen.jpg)

4 Click the **Setting** button to set columns.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/collumn.jpg)

- Tick the columns you do not want to display, click the **①** button
- Click the **②** button to drag to change the column display order
- Click the **③** button to pin the column

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/collumn-1.jpg)
  
## Evaluation Details

### Evaluation results

Click the **sys/id** on the evaluation table for the summary and detailed results.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/sysid.jpg)

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/eval-result.jpg)

### Evaluation Tasks and Logs
  
**Tasks**

Click the **Tasks** tab to see all the tasks of an evaluation.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/tasks.jpg)

**Logs**

Click the **View logs** button at the end of the task table to view logs.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/model/model%20eval/viewlog.jpg)
