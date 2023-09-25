# Deployments

1. How many Replicasets exist on the system?
```bash
kubectl get rs 
```

2. How many deployments exist in the system?
```bash
kubectl get deployments
```

3. Create a new Deployment using the ```deployment-definition-1.yaml``` file located at ```/root/```
```bash
kubectl apply -f <filename> # note the syntax could be wrong so look up docs to find what's wrong 
```

