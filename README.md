# k8s
This is a simple app managed using kubernetes

App Name: my-app.example

Docker Image: Nginx

- kind Pod -> pod.yml
- kind Replica Set -> replicaSet.yml
- kind Service -> service.yml
- kind Ingress -> ingress.yml
- kind Deployment -> deployment.yml


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

# Workflows

<img width="591" alt="Screenshot 2021-09-08 at 11 59 21 AM" src="https://user-images.githubusercontent.com/4533119/132458253-723d4ea0-eacb-4a37-bb49-e27c38974b9d.png">
<img width="593" alt="Screenshot 2021-09-08 at 12 00 08 PM" src="https://user-images.githubusercontent.com/4533119/132458276-5ee0e917-2248-4142-a1e5-2df17d866e01.png">
