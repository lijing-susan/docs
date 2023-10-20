---
title: Model Evaluation
---

## Create an Evaluation

1. Enter the evaluation list page and click the "**Create**" button located in the upper right corner.
2. Select and fill out the items on the creation page:
   - Select a "**template**" (optional): If you would like to use a template, select it from the dropdown menu. If you do not want to use a template, leave it blank.
   - Select a "**resource pool**": Different resource pools represent different computing resources.
   - Select a "**model version**" and "**handler**".
   - Select a "**dataset version**".
   - Select a "**runtime version**".
   - **Debug mode**: Debug mode is off by default. If you enable debug mode, please remember the debug password for future debugging.
   - **Automatic release**: The default automatic release time is 3,600 seconds. You can modify it to any other duration. If you set an automatic release, the system will automatically release the resources when the duration is reached and cancel the evaluation. If you do not set an automatic release, the system will run the evaluations until your account's available balance is 0 unless manually cancelled.
3. Confirm the resource cost and click "**Submit**" to run the evaluation.

## View Evaluation Tasks

The evaluation list page allows you to view all evaluations in the project. Evaluations run through the UI, CLI, and SDK will be displayed on the evaluation list page in chronological order from newest to oldest.

### Searching and Filtering Evaluations

#### Simple Search

The evaluation list page supports simple search, allowing you to filter evaluations by selecting "Evaluation Task Status", "Model Name", and "Model Version".

#### Advanced Search

The evaluation list supports querying evaluations through expressions.

1. Click "**Advanced Search**".
2. Enter the column name you would like to query in the search bar, select a comparison operator, and enter or check the corresponding content.
3. Click "**Done**" to filter evaluations based on your search criteria.

### Compare Evaluations

The evaluation list supports comparing the results of multiple evaluation tasks simultaneously, allowing you to identify the best-performing models easily.

1. Check the checkbox next to the evaluations you would like to compare to enter comparison mode. If you would like to exit comparison mode, uncheck the checkboxes.
2. The evaluation selected as the baseline evaluation is fixed. If you would like to change the baseline evaluation, pin another evaluation instead.
3. Click the "**Evaluation Details View**" button in the lower right corner to view the details difference in evaluations. You can switch between split-screen view and full-screen view.
4. Click the "**Column Management**" icon to customize the columns displayed in the list view. You can define which columns to display and hide, adjust their display order by dragging and dropping, and pin certain or multiple columns.

### Customized Evaluation View

Customized views allow your evaluation view to be more consistent with daily usage habits, facilitating the viewing and management of evaluations.

#### Create a Customized View

- **Save to Current View**: Click the "**Save**" button next to the customized view drop-down menu to save the current query conditions and column fields to the current view.
- **Save as New View**: Click the "**Save as**" button next to the customized view drop-down menu to save the current query conditions and column fields as a new view.
  1. Click the "**Save as**" button next to the customized view drop-down menu.
  2. Enter a "**View Name**".
  3. Set the columns to be visible or invisible; by default, all columns are visible.
  4. Select a sorting strategy; by default, evaluations are sorted by creation time in descending order.
  5. Click "**Save**" to complete the creation of the new view.

#### Edit a Customized View

1. Click "**Manage Views**" in the drop-down menu of the customized view.
2. Click "Edit".
3. Edit the items that need to be adjusted.
4. Click "**Save**" to complete the edit.

#### Delete a Customized View

1. Click "**Manage Views**" in the drop-down menu of the customized view.
2. Click "**Delete**".
3. Click "**Save**" to complete the deletion.

#### Set the Default View

1. Click "**Manage Views**" in the drop-down menu of the customized view.
2. Turn on the "**Default**" switch.
3. Click "**Save**" to complete the default view setting.

#### Set a View Invisible

If you would like to temporarily hide one or more views, you can follow these steps:

1. Click the "**Manage Views**" in the drop-down menu of the customized view.
2. Turn off the "Visible" switch; the view(s) will be invisible in the customized view drop-down menu. Turn on the "Visible" switch, the view(s) will be visible again;
4. Click "**Save**" to complete the visibility setting.

## View Evaluation Details

### View Evaluation Results

#### View Summary Result 

1. Enter the evaluation list page and click "**sys/id**".
2. Click the "**Overview**" tab to view the summary results of the evaluation.

#### View Detailed Results

1. Enter the evaluation list page and click "**sys/id**".
2. Click the "**Results**" tab to view the detailed results of the evaluation.

#### Customized Detailed Result Dashboard

- **Add a Panel**：Click the "**Add Panel**" button to add a new panel, or click the "Panel Settings" button and then click "Add a new panel above" or "Add a new panel below" to add a new panel above or below the current panel. Click the "**Save**" button in the upper right corner to save the changes.

- **Rename a Panel**：Click the "Panel Settings" button and then click "**Rename**", enter the panel name, then click the "**Submit**" button to rename the panel. Click the "**Save**" button in the upper right corner of the result tab to save the changes.

- **Delete a Panel**：Click the "**Panel Settings**" button and then click "**Delete**". Click "**Yes**" to confirm the deletion, or click "**No**" to cancel the deletion. Click the "**Save**" button in the upper right corner of the result tab to save the changes.

- **Add a Chart**：Click the "**Add Chart**" button in the panel's upper right corner, select the chart type, select the data table, select the metrics, enter the chart title, and then click "**Submit**" to submit the chart. Click the "**Save**" button in the upper right corner of the result tab to save the changes.

- **Edit a Chart**：Click the "**Settings**" icon in the upper right corner of the chart, click "**Edit Chart**", edit the content that needs adjustment, click "**Yes**" to confirm the editing or click "**No**" to cancel the editing. Click the "**Save**" button in the upper right corner of the result tab to save the changes.

- **Delete a Chart**：Click the "**Settings**" icon in the upper right corner of the chart, click "**Delete Chart**", click "**Yes**" to confirm the deletion or click "**No**" to cancel the deletion. Click the "Save" button in the upper right corner of the result tab to save the changes.

### View Evaluation Tasks and Logs

#### View Evaluation Tasks

1. Enter the evaluation list page and click "**sys/id**" to go to the evaluation details page.
2. Click on the "**Evaluation task**" tab to view all evaluation tasks of this evaluation.

#### View Evaluation Logs

1. Enter the evaluation list page and click "**sys/id**" to go to the evaluation details page.
2. Click on the "**Tasks**" tab and click on the "**View Logs**" icon to view logs.
