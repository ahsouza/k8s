# Orquestration containers with Kubernets

![alt text](https://cdn-images-1.medium.com/max/1200/1*A-kYNXMDiSLXde-ilVNJvg.png)


### Climbing pods

#### Applying ConfigMap

```sh
kubectl apply -f configmap.yaml
```

#### Verify with:

```sh
kubectl get configmaps
```

#### Applying Deployment

```sh
kubectl apply -f deployment.yaml
```
#### Veirfy Deployment:

```sh
kubectl get pods
```


#### Applying services

```sh
kubectl apply -f service.yaml
```


#### Show services

```sh
kubectl get svc
```

#### Simulating service with minikube

```sh
minikube service nginx-service
```

#### If you want to destroy the pods:

##### Delete pod selected

```sh
kubectl delete deployment ahsouza-nginx
```

##### Delete All

```sh
kubectl delete deployments --all
```
