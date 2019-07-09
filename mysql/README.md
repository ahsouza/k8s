### Applying deployment MYSQL

```sh
kubectl apply -f deployment.yaml
```

### Applying volume persistent

```sh
kubectl apply -f persistent-volume.yaml
```
#### Verify volume

```sh
kubectl get peristentvolumeclaim
```


### Verify pods

```sh
kubectl get pods
```