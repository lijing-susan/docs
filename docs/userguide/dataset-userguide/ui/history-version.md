---
title：History Version Management of a Starwhale Dataset
---

## History versions of a dataset {#history}

1 Click **Version History** to see all the history versions of a dataset.

![image](https://user-images.githubusercontent.com/101299635/234795306-7311c641-ca31-44ae-9c59-a3a66433285a.png)

2 Starwhale dataset history version list displays the basic dataset version information: Version name, version alias, whether the version is shared, the created time of the version and dataset version action.

![image](https://user-images.githubusercontent.com/101299635/234825710-37a13e18-7df1-471c-b339-445f49435c91.png)

:::catution
If a dataset version is shared, it is visible to anyone. If it is not shared,  it can only be seen and used by users with permission. 
:::

## Share a specific version of a dataset {#share}

1 Go to the **Overview** tab of the dataset detail page.

2 Click the designed button to switch the button to a shared mode(Shared = True), and then the dataset version is shared with all users of Starwhale. If you want to stop sharing, switch the button to an unshared mode((Shared = False). 

If the dataset is part of a public project, a shared dataset can be accessed and utilized by all users. For more information, see [Roles and permissions](https://doc.starwhale.ai/docs/concepts/roles-permissions)

:::catution
If a dataset version is shared, it is visible to anyone. If it is not shared,  it can only be seen and used by users with permission. 
:::

![image](https://user-images.githubusercontent.com/101299635/234837932-18a7270f-a1c5-48f6-8aec-5f58458d357c.png)

## Copy a specific version of a dataset to local {#copy}

1 Type command `sw assistance wait-console` in CLI to serve Starwhale.

![image](https://github.com/lijing-susan/docs/assets/101299635/63364c6c-92c7-4f1d-bd1d-216a19acb228)

2 Click the **Push to local** button to push a specific version of the dataset directly to your local environment.

![image](https://github.com/lijing-susan/docs/assets/101299635/0fb349ee-e275-4f20-98a8-d6924320c47b)
