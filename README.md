# K8s-Tutorial-Guestbook

This tutorial is based on K8s Official Tutorial:

Stateless Application

Example: Deploying PHP Guestbook application with Redis

https://kubernetes.io/docs/tutorials/stateless-application/guestbook/


## Procedure

### Start up the Redis Master
```
kubectl apply -f redis-master-deployment.yaml
kubectl apply -f redis-master-service.yaml
```

### Start up the Redis Slaves
```
kubectl apply -f redis-slave-deployment.yaml
kubectl apply -f redis-slave-service.yaml
```

### Set up and Expose the Guestbook Frontend
```
kubectl apply -f frontend-deployment.yaml
kubectl apply -f frontend-service.yaml
```

### Access the GuestBook

Use http://Node_IP:NodePort to access the GuestBook Application


### Scale the Web Frontend
```
kubectl scale deployment frontend --replicas=5

```
