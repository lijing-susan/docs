---
title: Install Starwhale Server with Helm
---

## Prerequisites

* A running Kubernetes 1.19+ cluster to run tasks.
* A running MySQL 8.0+ instance to store metadata.
* A S3-compatible object storage system to save datasets, models, and others.
* [Helm](https://helm.sh) 3.2.0+.

The Starwhale Helm Charts includes MySQL and [MinIO](https://min.io/) as dependencies. If you do not have your own MySQL instance or any S3-compatible object storage available, use the Helm Charts to install. Please check [Installation Options](#installation-options) to learn how to install Starwhale Server with MySQL and MinIO.

## Create a service account on Kubernetes for Starwhale Server

If Kubernetes RBAC is enabled (In Kubernetes 1.6+, RBAC is enabled by default), Starwhale Server can not work properly unless is started by a service account with at least the following permissions:

| Resource | API Group | Get | List | Watch | Create | Delete |
|----------|-----------|-----|------|-------|--------|--------|
| jobs     | batch     | Y   | Y    | Y     | Y      | Y      |
| pods     | core      | Y   | Y    | Y     |        |        |
| nodes    | core      | Y   | Y    | Y     |        |        |
| events   | ""        | Y   |      |       |        |        |

Example:

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

# Downloading Starwhale Helm Charts

```bash
helm repo add starwhale https://star-whale.github.io/charts
helm repo update
```

## Installing Starwhale Server

```bash
helm install starwhale-server starwhale/starwhale-server -n starwhale --create-namespace
```

If you have a local `kubectl` command-line tool installed, you can run `kubectl get pods -n starwhale` to check if all pods are running.

## Updating Starwhale Server

```bash
helm repo update
helm upgrade starwhale-server starwhale/starwhale-server
```

## Uninstalling Starwhale Server

```bash
helm delete starwhale-server
```
