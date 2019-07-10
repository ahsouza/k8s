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

# Kubernetes no GCP

![alt text](https://cdn-images-1.medium.com/max/1200/1*_saMmI_5Kse6rqZPkiekfg.png)

### Deploying resources
#### After connecting the cluster to GCP

ConfigMap NGINX

```sh
kubectl apply -f configmap.yaml
```

Applying deployment NGINX

```sh
kubectl apply -f deployment.yaml
```

Applying service LoadBalancer

```sh
kubectl apply -f service.yaml
```

Applying volume persistent, service and deployment of MySQL

```sh
cd mysql
kubectl apply -f persistent-volume.yaml
kubectl create secret generic mysql-pass --from-literal=password='@hs@hs@hs0uzA'
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```