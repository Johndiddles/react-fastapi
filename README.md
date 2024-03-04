# HELM CHART FOR REACT-FASTAPI-APP

## Requirements

[kubectl](https://kubernetes.io/docs/tasks/tools/), [ingress-nginx](https://kind.sigs.k8s.io/docs/user/ingress/#ingress-nginx), [helm](https://helm.sh/docs/intro/install/#from-script)

## How to deploy the chart

### Clone the repo

```git
    git clone https://github.com/Johndiddles/react-fastapi
```

### CD into the cloned repo

```bash
    cd react-fastapi
```

### Create namespace using

```bash
    kubectl create namespace helm-playground
```

### switch into the new namespace

```bash
    kubectl config set-context --current --namespace=helm-playground
```

### Deploy the ingress service

```bash
    kubectl apply -f ./nginx-ingress.yaml
```

### install chart

```bash
    helm install dev react-fastapi-api --values ./react-fastapi-cchart/values.yaml
```
