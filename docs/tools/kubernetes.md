# Kubernetes Cheat Sheet

Kubernetes (K8s) is a container orchestration platform.

## Basic kubectl Commands

| Command | Description |
| :--- | :--- |
| `kubectl get pods` | List all pods in the namespace |
| `kubectl get svc` | List all services |
| `kubectl get nodes` | List cluster nodes |
| `kubectl apply -f <file.yaml>` | Create/Update resources from a file |
| `kubectl delete -f <file.yaml>` | Delete resources defined in a file |
| `kubectl logs <pod>` | View logs of a pod |
| `kubectl exec -it <pod> -- bash` | Open a shell inside a pod |

## Simple Pod Definition

Save as `pod.yaml`:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
spec:
  containers:
  - name: nginx
    image: nginx:latest
    ports:
    - containerPort: 80
```

Apply it:

```bash
kubectl apply -f pod.yaml
```