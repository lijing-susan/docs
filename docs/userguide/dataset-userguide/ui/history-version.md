---
title: History Version Management of a Starwhale Dataset
---

## History versions of a dataset {#history}

1 Click **Version History** to see a dataset's history versions.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/history%20version/list1.png)

2 Starwhale dataset history version list displays the basic dataset version information: Version name, version alias, whether the version is shared, the created time of the version and dataset version action.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/history%20version/hslist.png)

:::catution
If a dataset version is shared, it is visible to anyone; Otherwise, users can only see and use it with permission. 
:::

## Share a specific version of a dataset {#share}

1 Go to the **Overview** tab of the dataset detail page.

2 Click the designed button to switch the button to a shared mode(Shared = True), and then the dataset version is shared with all users of Starwhale. If you want to stop sharing, switch the button to an unshared mode((Shared = False). 

All users can access and utilise a shared dataset if the dataset is part of a public project. For more information, see [Roles and permissions](https://doc.starwhale.ai/docs/concepts/roles-permissions)

:::catution
If a dataset version is shared, it is visible to anyone; Otherwise, users can only see and use it with permission. 
:::

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/history%20version/share.png)

## Copy a specific version of a dataset to local {#copy}

1 Type command `sw assistance wait-console` in CLI to serve Starwhale.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/history%20version/push%20to%20local.png)

2 Click the **Push to local** button to push a specific version of the dataset directly to your local environment.

![image](https://starwhale-examples.oss-cn-beijing.aliyuncs.com/docs/User%20guide/Dataset/history%20version/push%20conslole.png)
