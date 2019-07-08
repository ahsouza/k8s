### Running file pod

```sh
kubectl apply -f pod.yaml
```

#### Show pods

```sh
kubectl get pods
```


#### Creting deployment from pods
```sh
kubectl create deployment nginx-pod --image=nginx:1.17-alpine
```


#### Creting a service to access pods
```sh
kubectl expose deployment nginx-pod --type=LoadBalancer --port=80
```

#### Show services
```sh
kubectl get services
```

#### Simulating service with minikube
```sh
minikube service nginx-pod
```

#### Deleting deployment
```sh
kubectl delete deployments --all
```

### Creating and running file deployment

```sh
kubectl apply -f deployment.yaml
```

### Up services

```sh
kubectl apply -f service.yaml
```

### Show services

```sh
minikube service nginx-service
```