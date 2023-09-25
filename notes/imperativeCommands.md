# Imperative Commands 
> In this lab you will get hands on practice creating kubernetes objects imperatively 

1. Deploy a prod named ```nginx-pod``` using the ```nginx:alpine``` image 
```bash
1. create pod using the pod template yaml on the documentation
2. set the name and image to the correct requirements
kubectl apply -f <pod-definition.yaml> 
```

2. Deploy a ```redis``` pod using the ```redis:alpine``` image with the labels set to ```tier=db```
```bash
kubectl run redis --image=redis:alpine --dry-run=client -oyaml redis-pod.yaml
> then make the necessary edit to the file to have tier:db 

or 

kubectl run redis -l tier=db --image=redis:alpine
```

3. Create a service ```redis-service``` to expose the redis application within the cluster on port ```6379```
```bash
kubectl expose pod redis --port=6379 --name redis-service 
```