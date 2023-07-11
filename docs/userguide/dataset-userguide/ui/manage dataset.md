---
title: Manage a Starwhale Dataset by UI
---

## Starwhale Dataset list

Starwhale dataset list displays the basic dataset information: Dataset name, the latest dataset version alias, dataset owner, the created time and dataset actions.

![image](https://user-images.githubusercontent.com/101299635/234795143-2987043e-9dd2-4b73-8ff9-73b83762356e.png)

## Starwhale Dataset Detail Information

Dataset version information consists of three parts: Overview, metadata, and files.

**Overview** 

The basic information of a dataset version, including dataset name, dataset version name, dataset version aliases, whether the dataset version is shared, and the created time of a dataset version.

![image](https://user-images.githubusercontent.com/101299635/234795667-e2331a52-351d-4dcd-a5ad-631596cd2ea9.png)

:::caution
Switch the button to set a dataset version to a shared mode if the dataset belongs to a public project. A shared dataset can be seen and used for everyone. For more information, see [Roles and permissions](https://doc.starwhale.ai/docs/concepts/roles-permissions) 
:::

**Metadata**

The metadata of the dataset, including the building os information, Starwhale version information, and dataset summarized information.

![image](https://user-images.githubusercontent.com/101299635/234795955-337bd013-782b-48fd-97dc-1af9067ffc1a.png)

**Files**

Supporting viewing data like videos, images, audio, texts, and annotations.

| Data Types | Format | Annotation Types |
|---|---|---|
| Images |jpg, jpeg, png | 2D Box, 2D Polygon, 2D Polyline, 2D Keypoint, Classification, Segmentation |
| Videos | MP4 | Classification |
| Audios | MP3, wav | Classification |
| Texts | txt | Classification |

## Starwhale Dataset Visualization

### Image data viewer

Image data visualization support viewing image data in tables(default) or a larger view.

- **Table view**

  ![image](https://user-images.githubusercontent.com/101299635/234798959-ba214fb9-bf94-413b-b6b5-81d0d9f5ba40.png)

- **Full view**

  The left side of the full view displays the annotation information supporting choosing whether the annotations are to display or not.

  ![image](https://user-images.githubusercontent.com/101299635/234799661-9b33cf77-975f-40be-8f87-55a705848660.png)

### Video data viewer**
  
- **Table view**

  ![img_v2_9a04dddd-6c39-4b45-8763-075798f1e48g](https://user-images.githubusercontent.com/101299635/234829713-42ca7580-d2b6-4e98-b9d4-92f8c0e2585d.jpg)

- **Full view**

  Video data visualization support viewing audio data in tables(default) or a larger view.

  1 The left side of the full view displays the annotation information.

  2 The lower right corner can play/pause, play volume, play speed and play in full screen.

  ![img_v2_3e961d3c-4d57-42ff-b18a-1d9cf65db64g](https://user-images.githubusercontent.com/101299635/234829798-ea4f6cb2-3c88-43dd-88d9-55e43db3a95c.jpg)

### Audio data viewer
 
Audio data visualization support viewing audio data in tables(default) or a larger view.

- **Table view**

  ![image](https://user-images.githubusercontent.com/101299635/234803932-59089931-00c3-4d12-b101-5d4f11191df3.png)

- **Full view**

  1 The left side of the full view displays the annotation information

  2 The lower right corner can play/pause and play volume. Click More, can download and adjust the play speed.

  ![image](https://user-images.githubusercontent.com/101299635/234804126-3f6f76b0-95ba-4bf4-9150-6ee7c9563c54.png)

### Text data viewer

Text data visualization support viewing text data in tables(default) or a larger view

![image](https://user-images.githubusercontent.com/101299635/234797034-84f2c866-a06a-4552-a292-966d9e8522d5.png)

## Share a Starwhale Dataset 

Easily switch between shared and unshared modes for dataset versions by clicking the designated button. If the dataset is part of a public project, a shared dataset can be accessed and utilized by all users. For more information, see [Roles and permissions](https://doc.starwhale.ai/docs/concepts/roles-permissions)

![image](https://user-images.githubusercontent.com/101299635/234837932-18a7270f-a1c5-48f6-8aec-5f58458d357c.png)

## Remove a Starwhale Dataset

Click **Remove** first, then click **Yes** to confirm or click **No** to cancel.

:::caution
If you confirm to remove, all versions of a dataset will be removed.
:::

![image](https://github.com/lijing-susan/docs/assets/101299635/8cba965d-d634-4120-9c9a-e2a434503678)

![image](https://github.com/lijing-susan/docs/assets/101299635/eb306408-e0e1-4a76-8bde-37dc49e9b0ff)

## Recover a preciously removed Starwhale Dataset

You can go to **Trash** to find the dataset you want to recover, then click **Restore** to recover your datasets. And then, click **Yes** to confirm or click **No** to cancel.

![image](https://github.com/lijing-susan/docs/assets/101299635/d1640061-3ffb-472b-9fd8-a6d7601cb52a)

![image](https://github.com/lijing-susan/docs/assets/101299635/38a0d54e-3c1d-4781-9278-290a6018a21a)
