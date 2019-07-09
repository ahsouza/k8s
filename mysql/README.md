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


#### Generating key secret

```sh
kubectl create secret generic mysql-pass --from-literal=password='a1s2d3f4'
```

#### Verify secret

```sh
kubectl get secrets
```

### Verify pods

```sh
kubectl get pods
```