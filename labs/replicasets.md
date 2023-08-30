# Replica Sets labs

1. How many ReplicaSets exist on the system?
```bash
kubectl get rs 
# lists the number of replicasets that exist on the system
```

2. How many pods are desired in the replica set?

```bash
NAME              DESIRED   CURRENT   READY   AGE
new-replica-set   4 (pods)  4         0       15s
```

3. Kubectl describe replica sets 
```bash
kubectl describe rs/<replica-set-name>
```

4. Check number of pods ready in a replica-set
```bash
NAME                    READY   STATUS             RESTARTS   AGE
replica-set-kzn75   0/1     ImagePullBackOff   0          6m40s
replica-set-nj6bc   0/1     ImagePullBackOff   0          6m40s
# zero pods are ready, don't be careless
```

5. There are still 4 pods, after I have deleted one... why?
> replica sets always ensures that pods run 