## Setup

### Required Tools
minikube
helm (v3.9.1)
kustomize (v4.1.3)
kubectl (1.21)

### Install

1) Start minikube with following resource
```minikube start --kubernetes-version v1.21.1 --cpus 4 --memory 8192 --driver=hyperkit```

2) Enable nginx addon
```minikube addons enable ingress```

3) Allow k8s resources on minikube can access internet
https://github.com/kubernetes/minikube/issues/1340#issuecomment-903254447

4) Clone this repo to local & issue following to command to install all the resources
```kustomize build . | kubectl apply -f -```

