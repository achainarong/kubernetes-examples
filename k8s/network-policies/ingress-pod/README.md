# Network policies with pod selectors

## Deploy network policies

```shell

  kubectl apply -k ./k8s/network-policies/ingress-pod

```

## Delete network policies

```shell

  kubectl delete -k ./k8s/network-policies/ingress-pod

```

## How to connect to one of the postgres-clients

```shell

  kubectl exec good -n network-demo -it -- "/bin/sh"
  kubectl exec bad -n network-demo -it -- "/bin/sh"

  # testing the connectiong
  psql -U postgres -h db-service test

```
