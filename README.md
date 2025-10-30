## Understanding Kubernetes from beginner POV

**Problem Statement** : Creating a simple Nginx pod manually via YAML.


**Necessary Commands** to run

```bash
kubectl apply -f testing-pod.yaml
```

Check the pod status

```bash
kubectl get pods
```

Check the pod details

```bash
kubectl describe pod testing-pod
```

See the status of Node, Pod IP, Events and Container Info


View complete logs from the container

```bash
kubectl logs testing-pod
```


Exposing the pod via port-forwarding

```bash
kubectl port-forward pod/testing-pod 8080:80
```

In order to delete the pod

```bash
kubectl delete pod testing-pod
```



### Understanding the Yaml

- `apiVersion:v1` - Specifies the Kubernetes API version being used.For basic Pod definitions, the version is v1.

- `kind: Pod` - Defines the type of Kubernetes object. Here, it creates a Pod, the smallest deployable unit in Kubernetes.

- `metadata`  - Contains identifying information about the Pod, like its name and labels.

- `spec` - Defines the desired behavior or configuration of the Pod.

- `containers` - list the containers which run inside the Pod
