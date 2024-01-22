# Kubernetes and Helm Quick Instructions

## Set Up Aliases:

```bash
alias k=kubectl
```

## Port Forwarding and Minikube Tunnel:
k port-forward 8080:80
minikube tunnel

## View Kubernetes Resources:
k get all


# Helm Commands:

## Install Helm Chart:
helm install webapp-release webapp1/

## List Helm Releases:
helm ls

## Upgrade Helm Release:
helm upgrade webapp-release webapp1/ --values webapp1/values.yaml

## Create Kubernetes Namespaces:
kubectl create namespace dev
kubectl create namespace prod

# Helm Installations in Different Environments:

## Dev Environment:
helm install mywebapp-release-dev ./webapp1 --values ./webapp1/values.yaml -f ./webapp1/values-dev.yaml -n dev

## Prod Enviroment:
helm install mywebapp-release-prod ./webapp1 --values ./webapp1/values.yaml -f ./webapp1/values-prod.yaml -n prod
