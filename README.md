# ENSF-400-Assignment-3
---

## Run the following commands in order...

### minikube
```
minikube start
minikube addons enable ingress
```

### nginx
```
kubectl apply -f nginx-configmap.yaml
kubectl apply -f nginx-dep.yaml
kubectl apply -f nginx-svc.yaml
kubectl apply -f nginx-ingress.yaml
```

### app1
```
kubectl apply -f app-1-dep.yaml
kubectl apply -f app-1-svc.yaml
kubectl apply -f app-1-ingress.yaml
```

### app2
```
kubectl apply -f app-2-dep.yaml
kubectl apply -f app-2-svc.yaml
kubectl apply -f app-2-ingress.yaml
```

---

## Curl
```
curl http://$(minikube ip)/
```

Note: You may have to wait a little for it to properly set up
