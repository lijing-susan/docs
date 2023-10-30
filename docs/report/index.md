---
title: Report Management
---
Starwhale's Report is a rich text editor that allows you to present the model evaluation results in document form and share the reports.

## View a Report

### View Reports list

Click the **Report** icon on the left navigation bar to enter the report list page and view all reports under the project.

### View Report details

Click the **Report title** or **Preview** to view the report's details.

## Create a Report

Click the **Create** button on the top right of the report list page to create a new report.

## Editing and Layout

In Starwhale's Report, we use "blocks" to refer to structured elements. Each type of content in the report is a "block", including text, headings, code, panels, etc.

You can insert "blocks" while editing a report to create a satisfactory report.

Type **/** into a blank line in a report or an appropriate location in the main text, and trigger the **Quick Insert** by pressing ** / **. Then, select the desired "block" from the toolbar menu. 

### Inserting Text

Type **/** into a blank line in the report or an appropriate location in the main text, and trigger the **Quick Insert** by pressing ** / **. Then select **Text** from the toolbar menu.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/report/text.jpg)

### Inserting a Table of Content

**Inserting a Table of Content**: Type **/** into a blank line in the report or an appropriate location of the text, and trigger the **Quick Insert** by pressing ** / **. Then select **Title Level** from the toolbar menu to insert it.

**Convert to a Table of Contents**: Hover the mouse over a line of text and select the **Heading Level** from the T⋮⋮ toolbar on the left side of the report to convert this text into a heading.

### Numbered List and Bullet List

Type / into an empty line in the report or an appropriate location of the text, and trigger the **Quick Insert** by pressing ** / **. Then select **Numbered List** or **Bullet List** from the toolbar menu.

### Inserting a Code Block

**Inserting a Code Block**: Type **/** into an empty line in the report or an appropriate location of the text, and trigger the **Quick Insert** by pressing ** / **. Then select **Code Block** from the toolbar menu.

**Converting to a Code Block**: Hover over the text and select **Code Block** from the **T⋮⋮ toolbar** on the left of the report to convert this text into a code block.

### Using Quotes in Reports

Type **/** into a blank line in the report or an appropriate location of  text, and trigger the **Quick Insert** by pressing ** / **. Then select **Quote** from the toolbar menu.

### Insert a Panel and Evaluation Data

Here are the main steps for inserting panels and evaluation data

1. Insert and edit a panel
2. Add and edit evaluation data
3. Add and edit charts

#### Insert and Edit Panel

**Insert a panel**: Type **/** in a blank line of the report or a location of the text, and you can trigger "Quick Insertion". Select **Panel** from the toolbar menu to insert it. 

**Rename a panel**: Click the **Settings** button on the top right corner of the panel, select **Rename** from the drop-down menu, enter a new name from the pop-up window, and click the **Submit** button.

**Delete a panel**: Click the **Settings** button on the top right corner of the panel, select **Delete** from the drop-down menu, and then click the **Yes** button on the pop-up window to delete the selected panel. 

#### Add Evaluation Data

**Add evaluation**: Click the **Add Evaluation** button on the right side of the evaluation list, select the data you want to display and click the **Add** button. It supports selecting evaluation data across projects by switching projects in the selection menu.

**Remove an evaluation**: Click the **Remove** button before the added evaluation to remove selected evaluation data.

**Columns setting**: Click the **Column Management** button on the right side of the evaluation list to set the columns's visibility in the evaluation table. You can define which columns should be displayed/hidden, adjust their display order (by dragging), and fix certain columns.

#### Add Charts

**Add a chart**: Click the **Add Chart** button on the right side of the evaluation list, and then select the chart type, data table, and data displayed on X-Axis and Y-Axis, enter the chart name, and click the **Submit** button to add the chart.

Note: There is an association between the evaluation table list and charts. The data range selected from the evaluation list is the maximum data range that can be selected for the chart.

**Change the size of a chart**: You can hover over the bottom right corner of the chart and drag to edit the chart size to what you like.

**Edit a chart**:  Click the **Settings** button at the top right corner of a chart, and select the **Edit Chart** from the drop-down menu to edit the chart type, data, and chart name. Click **Submit** to save the edited content.

**Delete a chart**: Click the **Settings** button at the top right corner of a chart, and select the **Delete** from the drop-down menu, then click the **Yes** button in the pop-up window to delete the chart.

## Publish a Report

Click the **Publish to Report** button on the top right of the report to publish the latest edited content of the report. 

:::
caution: The edited content will automatically be saved locally, which means it only temporarily stores the edited content locally. The content may be lost if it is not published to the project.
:::

## Sharing and Permissions

Click the **Share** switch on the report list page to share the report with anyone who gets the report link. The report's URL will be automatically copied when you switch on the **Share** button.

## Preview a Report

Click the "Preview" button on the report list page to preview the report.

## Copy a Report Link

Click the "Copy Link" button on the report list page to copy the report link.

## Remove a Report

Click the **Remove** button on the report list page to move the report to the recycle bin. For more information on operation permissions, please refer to [Starwhale's Roles and Permissions](https://starwhale.cn/docs/concepts/roles-permissions).

## Restore a Report

Click the **Recycle Bin** icon on the left navigation bar to enter the recycle bin list. Click the **Restore** button and then the "Yes" button in the confirmation pop-up to restore the report. For more information on operation permissions, please refer to [Starwhale's Roles and Permissions](https://starwhale.cn/docs/concepts/roles-permissions).
