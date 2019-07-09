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
kubectl create secret generic mysql-pass --from-literal=password='@hs@hs@hs0uzA'
```

#### Verify secret

```sh
kubectl get secrets
```

### Verify pods

```sh
kubectl get pods
```

### Applying service to MySQL Server

```sh
kubectl apply -f service.yaml
```
#### Verify services

```sh
kubectl get svc
```
##### Running pod interactive:

```sh
kubectl exec -it <name_pode> bash
```


#### If you want to destroy the volume persistent:

##### Delete volume persistent with:

```sh
kubectl delete peristentvolumeclaim mysql-pv-claim
```