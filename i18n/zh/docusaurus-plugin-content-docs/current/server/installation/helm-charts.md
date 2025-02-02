---
title: 使用 Helm 安装 Starwhale Server
---

## 先决条件

* 1.19或者更高版本的Kubernetes集群用于执行任务。
* MySQL 8.0以上版本的数据库实例用于存储元数据。
* 兼容S3接口的对象存储，用于保存数据集、模型等。
* [Helm](https://helm.sh) 3.2.0+。

Starwhale Helm charts 包括 MySQL 和 [MinIO](https://min.io/) 作为依赖项。如果您没有自己的 MySQL 实例或任何与 AWS S3 兼容的对象存储可用，可以通过 Helm Chats 进行安装。请查看下文的[安装选项](#安装选项)以了解如何在安装 Starwhale Server 的同时安装 MySQL 和 MinIO。

## 在 Kubernetes 上为 Starwhale Server 创建一个服务账号

如果您的 Kubernetes 集群启用了 RBAC（在 Kubernetes 1.6+中，默认启用 RBAC），Starwhale Server 将无法正常工作，除非由至少具有以下权限的服务帐户启动：

| Resource | API Group | Get | List | Watch | Create | Delete |
|----------|-----------|-----|------|-------|--------|--------|
| jobs     | batch     | Y   | Y    | Y     | Y      | Y      |
| pods     | core      | Y   | Y    | Y     |        |        |
| nodes    | core      | Y   | Y    | Y     |        |        |
| events   | ""        | Y   |      |       |        |        |

例子：

```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRole
metadata:
  name: starwhale-role
rules:
- apiGroups:
  - ""
  resources:
  - pods
  - nodes
  verbs:
  - get
  - list
  - watch
- apiGroups:
  - "batch"
  resources:
  - jobs
  verbs:
  - create
  - get
  - list
  - watch
  - delete
- apiGroups:
  - ""
  resources:
  - events
  verbs:
  - get
  - watch
  - list
---
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRoleBinding
metadata:
  name: starwhale-binding
roleRef:
  apiGroup: rbac.authorization.k8s.io
  kind: ClusterRole
  name: starwhale-role
subjects:
- kind: ServiceAccount
  name: starwhale
```

## 下载 Starwhale Helm chart

```bash
helm repo add starwhale https://star-whale.github.io/charts
helm repo update
```

## 安装Starwhale Server

```bash
helm install starwhale-server starwhale/starwhale-server -n starwhale --create-namespace
```

如果您安装了`kubectl`命令行工具，您可以运行 `kubectl get pods -n starwhale` 来检查是否所有 pod 都在正常运行中。

## 更新 Starwhale Server

```bash
helm repo update
helm upgrade starwhale-server starwhale/starwhale-server
```

## 卸载 Starwhale Server

```bash
helm delete starwhale-server
```
