# k8s
This is a simple app managed using kubernetes

App Name: my-app.example
Docker Image: Nginx

1. kind Pod -> pod.yml
2. kind Replica Set -> replicaSet.yml
3. kind Service -> service.yml
4. kind Ingress -> ingress.yml
5. kind Deployment -> deployment.yml


### Commands:

1. Spin up pods locally using minikube
```
minikube status
minikube start
```
2. Spin up a pod
```
kubectl get pods
kubectl apply -f pod.yml
```

3. Spin up replica set of 3
```
kubectl get replicasets
kubectl apply -f replicaSet.yml
```

4. Spin up service
```
kubectl get replicasets
kubectl apply -f service.yml
```

5. Spin up ingress controller
```
kubectl get ingress
kubectl apply -f ingress.yml
```

6. Spin up deployment for auto updates and rollbacks
```
kubectl get deployments
kubectl apply -f deployment.yml
```

## To find IP of the app service

```
minikube ip
```

## To Test

```
kubectl run --rm --it --image-alpine my-test
apk -U add curl
curl -v app-service or curl -X GET http://<ip-address>/
```

## To change deployment

```kubectl edit deployment pod-deployment```

## To rollback

```kubectl rollout undo deployment/pod-deployment```
