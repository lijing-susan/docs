---
title: Starwhale Model User Guide
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

A Starwhale Model is a standard format for packaging machine learning models that can be used for various purposes, like model finetuning, model evaluation, and online serving. A Starwhale Model contains the model file, inference codes, configuration files, and any other files required to run the model.

For more information about the packaging format, see [the storage format](#format).

## Create a Starwhale Model

There are two ways to create a Starwhale Model: by [SWCLI](../reference/swcli/model.md) or by SDK.

<Tabs groupId="operating-mode">
  <TabItem value="cli" label="CLI">To create a Starwhale Model by SWCLI, you need to define a model.yaml, which describes some required information about the model package, and run the following command:
```bash
swcli model build <path to your model.yaml directory>
```
For more information about the command and model.yaml, see [the SWCLI reference](../reference/swcli/model.md#build).</TabItem>
  <TabItem value="sdk" label="SDK">macOS is macOS.</TabItem>
</Tabs>

<Tabs groupId="non-sdk-operating-mode">
  <TabItem value="cli" label="CLI">Windows is windows.</TabItem>
  <TabItem value="ui" label="UI">Unix is unix.</TabItem>
</Tabs>

### Create a Starwhale Model by SWCLI

To create a Starwhale Model by SWCLI, you need to define a model.yaml, which describes some required information about the model package, and run the following command:

```bash
swcli model build <path to your model.yaml directory>
```

For more information about the command and model.yaml, see [the SWCLI reference](../reference/swcli/model.md#build)

### Create a Starwhale Model by SDK

## Model Management

### Model Management by SWCLI
