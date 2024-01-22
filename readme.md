# Kubernetes and Helm Quick Instructions

**Navigation and Commands**

Shortcuts for `kubectl` and `helm`:

```bash
alias k=kubectl
alias h=helm
```

**Port Forwarding and Access**

- Forward local port 8080 to container port 80: `k port-forward 8080:80`
- Enable external access to LoadBalancer services with Minikube Tunnel: `minikube tunnel`

**View Kubernetes Resources**

- List all resources in the default namespace: `k get all`

**Helm Chart Management**

- Install a Helm chart: `h install <chart-name> <directory>`
- List all Helm releases: `h ls`
- Upgrade a Helm release: `h upgrade <release-name> <directory> --values <values-file>`

**Namespaces for Isolation**

- Create a namespace: `k create namespace <namespace-name>`
- Develop in `dev` and deploy in `prod` using values files:
  - Dev: `h install mywebapp-release-dev ./webapp1 --values ./webapp1/values.yaml -f ./webapp1/values-dev.yaml -n dev`
  - Prod: `h install mywebapp-release-prod ./webapp1 --values ./webapp1/values.yaml -f ./webapp1/values-prod.yaml -n prod`
