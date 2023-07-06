---
title: Starwhale Model User Guide
---

A Starwhale Model is a standard format for packaging machine learning models that can be used for various purposes, like model finetuning, model evaluation, and online serving. A Starwhale Model contains the model file, inference codes, configuration files, and any other files required to run the model.

For more information about the packaging format, see [the storage format](#format).

## Create a Starwhale Model

There are two ways to create a Starwhale Model: by [SWCLI](../reference/swcli/model.md) or by SDK.

### Create a Starwhale Model by SWCLI

To create a Starwhale Model by SWCLI, you need to define a model.yaml, which describes some required information about the model package, and run the following command:

```bash
swcli model build <path to your model.yaml directory>
```

For more information about the command and model.yaml, see [the SWCLI reference](../reference/swcli/model.md#build)

### Create a Starwhale Model by SDK

## Model Management

### Model Management by SWCLI

| Command | Description |
| ------- | ----------- |
| [`swcli model list`](../reference/swcli/model.md#list) | List all Starwhale Models in a project |
| [`swcli model info`](../reference/swcli/model.md#info) | Show detail information about a Starwhale Model |
| [`swcli model copy`](../reference/swcli/model.md#copy) | Copy a Starwhale Model to another location |
| [`swcli model remove`](../reference/swcli/model.md#remove) | Remove a Starwhale Model |
| [`swcli model recover`](../reference/swcli/model.md#recover) | Recover a previously removed Starwhale Model |

### Model Management by WebUI

- **Model List**
  
  Starwhale model list displays the basic information of a model: Model name, model owner, the latest model version alias, the created time, and model actions.

 ![image](https://github.com/lijing-susan/docs/assets/101299635/885ae4f9-9f6e-4f6d-8f63-2c0ec902c2ca)

- **Model Detail Information**
  
  Model version information consists of two parts: Overview and files.

  **Overview**: The basic information of a model version, including model name, model version name, model version aliases, and the created time of a model version.

  ![image](https://github.com/lijing-susan/docs/assets/101299635/7bc6b6df-dfd1-411a-b37c-66d8ae212fdf)
  
  **Files**: Support viewing model files.

  ![image](https://github.com/lijing-susan/docs/assets/101299635/6e16250b-e21f-4ed6-98f2-55ba32ce7e67)

- **Remove a Model**

  Click **Remove** to remove the model to trash.

  :::caution
  
  If you confirm to remove, all versions of a model will be removed.
  
  :::

  ![image](https://github.com/lijing-susan/docs/assets/101299635/a0691d1f-5c7b-45ba-b33b-f00d21ae20ec)

- **Recover a Model**
  
  You can go to **Trash** to recover your models.
  
  ![image](https://github.com/lijing-susan/docs/assets/101299635/3dcacd14-1d89-4457-bfd2-255ca104e272)

- **Delete a Model**

  Click **Remove** to remove the model to trash.  

  :::danger
  
  If you confirm to delete, all versions of a model will be deleted and will not be recovered any more.
  
  :::

  ![image](https://github.com/lijing-susan/docs/assets/101299635/9c6e7a4e-9e3a-452b-8038-04fea20b8e05)
  
## Model History

Starwhale Models are versioned. The general rules about versions are described in [Resource versioning in Starwhale](../concepts/versioning.md).

### Model History Management by SWCLI

| Command | Description |
| ------- | ----------- |
| [`swcli model history`](../reference/swcli/model.md#list) | List all versions of a Starwhale Model |
| [`swcli model info`](../reference/swcli/model.md#info) | Show detail information about a Starwhale Model version |
| [`swcli model diff`](../reference/swcli/model.md#diff) | Compare two versions of a Starwhale model |
| [`swcli model copy`](../reference/swcli/model.md#copy) | Copy a Starwhale Model version to a new one |

### Model History Management by WebUI

- **History Versions of a Model**

  1 Click **Version History** to see all the history versions of a model.

  ![image](https://user-images.githubusercontent.com/101299635/236391862-ef6b8905-e9e5-4781-b92c-43e276e7bf84.png)

  2 Starwhale model history version list displays the basic model version information: Version name, version alias, the created time of the version, and model version action.

  ![image](https://user-images.githubusercontent.com/101299635/236392797-b2582a8e-e1dc-46a1-8e63-5f263f9bac6d.png)

- **Switch to a Specific Version**

  Click the droplist to switch to the specific version

  ![image](https://user-images.githubusercontent.com/101299635/236405873-658fd8a6-2b3d-4c7a-922a-06af3eb74df8.png)

- **Identify the Differences between Versions of a Model**

   Switch the **Compare** button to open to view the difference between model versions

   ![img_v2_aa7d2887-736a-4484-be52-52512d150f9g](https://user-images.githubusercontent.com/101299635/236408520-6f165c5a-dd68-477b-a137-a005696c2d27.jpg)

## Model Evaluation

### Model Evaluation by SWCLI

| Command | Description |
| ------- | ----------- |
| [`swcli model eval`](../reference/swcli/model.md#eval) | Create an evaluation with a Starwhale Model |

### Model Evaluation by WebUI

- **Create a Model EValuation**

  1 Click **Create** to start configuring a model run.

  ![image](https://github.com/lijing-susan/docs/assets/101299635/6bf68f43-0ec0-406d-bbb7-6e9351457c25)

  2 Select the items on the page, and then Click **Submit** to create an evaluation.

- **Evaluation List**

  In the evaluation table, you can see all the evaluations of one project in one place.

  Each time you run an evaluation with Starwhale Web UI, Starwhale Client or Python SDK, it's added to the top of the table.

  ![image](https://github.com/lijing-susan/docs/assets/101299635/24087224-c0f2-40db-a565-5a79f2f0db35)

- **Side-by-Side Comparison of Evaluations**

  Select evaluations to compare by clicking the checkbox to include or exclude evaluations.
  
  [补动图]
  
- **Evaluation Result**

  [补动图]

- **Evaluation Tasks and Logs**
  
  **Tasks**

  Click **Tasks** tab to see all the tasks of an evaluation, or click a specific bar in the DAG to go to the task table.

  ![image](https://github.com/lijing-susan/starwhale/assets/101299635/2f580fa4-868e-4d8d-b14a-ea72396fd757)

  **Logs**

  Click **View logs** button at the end of the task table to view logs.

  ![image](https://github.com/lijing-susan/starwhale/assets/101299635/f1b896a7-f55b-40c9-a419-f44e0a3575fa)

## The Storage Format {#format}

The Starwhale Model is a tarball file that contains the source directory.
