## Problem
When following the instructions on [creating kustomization.yaml file](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/#create-a-kustomization-yaml) on the Kubernetes webpage, it suggests adding a Secret Generator using a cat command:
![1](./images/05-kustomization-file-secret-generator.jpg)

However, when deploying the file using `kubectl` command, it complains on validating data:

![6](./images/06-kustomization-file-secret-generator.jpg)

## Solution
Use the `Secret` kind in the kustomization.yaml file instead of the `Secret Generator`.

```
---
apiVersion: v1
kind: Secret
metadata:
  name: mysql-pass
type: Opaque
data:
  password: <PASSWORD>
```
