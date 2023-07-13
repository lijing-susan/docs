---
CLI User Guide of Starwhale Dataset 
---

Starwhale Dataset is a unified description of how the data and labels are stored and organized. Datasets are the most commonly used data in algorithm research, Starwhale Dataset can be easily accessed for Natural Language Processiong (NLP),Computer Vision, Audio and Radio tasks.

## Create a Starwhale Dataset(更新create相关命令链接)

| Command | Description | 
| ------- | ----------- |
| [`swcli dataset build --yaml /path/to/dataset.yaml`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from `dataset.yaml` |
| [`swcli dataset build --handler mnist.dataset:iter_mnist_item`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from handler |
| [`swcli dataset build --handler mnist.dataset:iter_mnist_item /path/to/dataset.yaml`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from handler |
| [`swcli dataset build --image-folder /path/to/image/folder`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from folder |
| [`swcli dataset build --video-folder /path/to/video/folder`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from folder |
| [`swcli dataset build --audio-folder /path/to/audio/folder`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from folder |
| [`swcli dataset build --json-file /path/to/example.json`](../reference/swcli/dataset#overview) | Create a Starwhale Dataset from json file |

## Manage a Starwhale Dataset

| Command | Description |
| ------- | ----------- |
| [`swcli dataset list`](../reference/swcli/dataset#list) | List all Starwhale Datasets in a project |
| [`swcli dataset info`](../reference/swcli/dataset#info) | Show detail information about a Starwhale Dataset |
| [`swcli dataset copy`](../reference/swcli/dataset#copy) | Copy a Starwhale Dataset between Standalone Instance and Cloud Instance |
| [`swcli dataset diff`](../reference/swcli/dataset#diff) | Compare two versions of a Starwhale Dataset |
| [`swcli dataset remove`](../reference/swcli/dataset#remove) | Remove a Starwhale Dataset |
| [`swcli dataset recover`](../reference/swcli/dataset#recover) | Recover a preciously removed Starwhale Dataset |

## Starwhale Dataset History Management

| Command | Description |
| ------- | ----------- |
| [`swcli dataset history`](../reference/swcli/dataset#history) | List all history versions of a Starwhale Dataset |
| [`swcli dataset info`](../reference/swcli/dataset#info) | Show detail information about a Starwhale Dataset |
| [`swcli dataset copy`](../reference/swcli/dataset#copy) | Copy a Starwhale Dataset version to a new one |
| [`swcli dataset diff`](../reference/swcli/dataset#diff) | Compare two versions of a Starwhale Dataset |
