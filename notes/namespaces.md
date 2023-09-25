# Namespaces 

1. Get the number of namespaces 
```bash
kuebctl get namespace 
```

2. Get number of pods based on a namespace 
```bash
kubectl get pods --namespace=<namespace_name>
```

3. Create a pod in a namespace 
```bash
kubectl run <name> --image=<image_name> -n finance
```

4. Watch the videos for the FQDN stuff, I don't understand it 