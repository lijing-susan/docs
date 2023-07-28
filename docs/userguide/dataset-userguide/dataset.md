---
User Guide of Starwhale Dataset 
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Create a Starwhale Dataset

<Tabs groupId="operating-way">
  <TabItem value="cli" label="CLI">
    | Command | Description | 
    | ------- | ----------- |
    | [`swcli dataset build --yaml /path/to/dataset.yaml`]((../reference/swcli/dataset#overview) | Create a Starwhale Dataset from `dataset.yaml` |
    | [`swcli dataset build --handler mnist.dataset:iter_mnist_item`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from handler |
    | [`swcli dataset build --handler mnist.dataset:iter_mnist_item /path/to/dataset.yaml`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from handler |
    | [`swcli dataset build --image-folder /path/to/image/folder`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from folder |
    | [`swcli dataset build --video-folder /path/to/video/folder`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from folder |
    | [`swcli dataset build --audio-folder /path/to/audio/folder`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from folder |
    | [`swcli dataset build --json-file /path/to/example.json`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from json file |
  </TabItem>
  <TabItem value="ui" label="UI">
    【待补充.】
  </TabItem>
</Tabs>

## Manage a Starwhale Dataset

<Tabs groupId="operating-way">
  <TabItem value="cli" label="CLI">
    | Command | Description |
    | ------- | ----------- |
    | [`swcli dataset list`](../reference/swcli/dataset#list) | List all Starwhale Datasets in a project |
    | [`swcli dataset info`](../reference/swcli/dataset#info) | Show detail information about a Starwhale Dataset |
    | [`swcli dataset copy`](../reference/swcli/dataset#copy) | Copy a Starwhale Dataset between Standalone Instance and Cloud Instance |
    | [`swcli dataset diff`](../reference/swcli/dataset#diff) | Compare two versions of a Starwhale Dataset |
    | [`swcli dataset remove`](../reference/swcli/dataset#remove) | Remove a Starwhale Dataset |
    | [`swcli dataset recover`](../reference/swcli/dataset#recover) | Recover a preciously removed Starwhale Dataset |
  </TabItem>
  <TabItem value="ui" label="UI">
    | Operation | Description |
    | ------- | ----------- |
    | [Dataset list](../userguide/dataset-userguide/ui/manage dataset.md#list) | List all Starwhale Datasets of a project on dataset page |
    | [Dataset detail information](../userguide/dataset-userguide/ui/manage dataset.md#list#info) | Show detail information about a Starwhale Dataset |
    | [Dataset visualization](../userguide/dataset-userguide/ui/manage dataset.md#visualize) | Interactively friendly view NLP, computer vision, audio and video data |
    | [Share a dataset](../userguide/dataset-userguide/ui/manage dataset.md#share) | Share a dataset to all Starwhale users |
    | [Remove a dataset](../userguide/dataset-userguide/ui/manage dataset.mdt#remove) | Remove a Starwhale Dataset |
    | [Recover a dataset](../userguide/dataset-userguide/ui/manage dataset.md#recover) | Recover a preciously removed Starwhale Dataset |
  </TabItem>
</Tabs>

## Manage History Versions of a Starwhale Dataset

<Tabs groupId="operating-way">
  <TabItem value="cli" label="CLI">
    | Command | Description |
    | ------- | ----------- |
    | [`swcli dataset history`](../reference/swcli/dataset#history) | List all history versions of a Starwhale Dataset |
    | [`swcli dataset info`](../reference/swcli/dataset#info) | Show detail information about a Starwhale Dataset |
    | [`swcli dataset copy`](../reference/swcli/dataset#copy) | Copy a Starwhale Dataset version to a new one |
    | [`swcli dataset diff`](../reference/swcli/dataset#diff) | Compare two versions of a Starwhale Dataset |
  </TabItem>
  <TabItem value="ui" label="UI">
    | Operation | Description |
    | ------- | ----------- |
    | [History list](../userguide/dataset-userguide/ui/history-version.md#history) | List all history versions of a Starwhale Dataset |
    | [Share a specific version of a dataset](../userguide/dataset-userguide/ui/history-version.md#share) | Share a specific version of a dataset to all Starwhale users |
    | [Copy a specific version of a dataset to local](../userguide/dataset-userguide/ui/history-version.md#copy) | Copy a specific version of a dataset to local with one click |</TabItem>
</Tabs>
