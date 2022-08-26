# Quickstart to test some examples

## Install minikube

macOS:

```shell
  brew install minikube
```

# Starting minikube

```shell

  # Using calico to write network policies
  minikube start --cni calico

```

## Deploy network policies

```shell

  kubectl apply -k ./k8s/network-policies/deployment

```

## Delete network policies

```shell

  kubectl delete -k ./k8s/network-policies/deployment

```

## How to connect to one of the postgres-clients

```shell

  kubectl exec good -n network-demo -it -- "/bin/sh"
  kubectl exec bad -n network-demo -it -- "/bin/sh"

  # testing the connectiong
  psql -U postgres -h db-service test

```
