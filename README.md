# My DevOps

## Minikube

```Bash
minikube start --cpus 4 --memory 8192
minikube ip
```

## Kubernetes CMD

```bash
kubectl get pod
kubectl get service
kubectl exec [pod] -- bash
kubectl logs [pod] -n [namespace]
kubectl describe pod [pod] -n [namespace]
```

## Initial setup

```bash
kubectl create namespace devops-tools
```

## Postgresql

Install [PgAdmin4](https://www.pgadmin.org/download/pgadmin-4-apt/)

```bash
kubectl apply -f postgresql/configmap.yaml
kubectl apply -f postgresql/deployment.yaml
kubectl apply -f postgresql/service.yaml
```

## Gitlab

```Bash
kubectl apply -f gitlab/gitlab.yaml
minikube service gitlab-service --url
```

## Jenkins

```Bash
kubectl apply -f jenkins/serviceAccount.yaml
kubectl apply -f jenkins/deployment.yaml
kubectl apply -f jenkins/service.yaml
```