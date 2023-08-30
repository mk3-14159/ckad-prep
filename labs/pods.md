# Pods lab 

1. Check number of pods 
```bash
kubectl get pods 
```

2. Create a new pod with the <image_name> image 
```bash
kubectl run <image> --image=<image>
kubectl run nginx --image=nginx
```

3. Find the image used to create the new pods 
```bash
kuebctl describe pod newpods-<new-pod-id>
```

4. Find out how many containers are part of the pod <pod-name>
```bash
kubectl describe pod <pod-name>
# information is shown under the containers tag
```

5. Deleting a <pod-name> pod 
```bash
kubectl delete pod <pod-name>
```

6. Creating a new pod with the name <new_name> and the image <new_image>
```bash
kubectl run <new_name> --image=<new_image> --dry-run=client -o yaml > <new_name>-definition.yaml
kubectl create -f <new_name>-definition.yaml
kubectl get pods
```