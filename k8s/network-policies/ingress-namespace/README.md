# Network policies with namespace selectors

## Deploy network policies

```shell

  kubectl apply -k ./k8s/network-policies/ingress-namespace

```

## Delete network policies

```shell

  kubectl delete -k ./k8s/network-policies/ingress-namespace

```

## How to connect to one of the postgres-clients

```shell

  kubectl exec good -n network-good -it -- "/bin/sh"
  kubectl exec bad -n network-bad -it -- "/bin/sh"

  # testing the connectiong
  psql -U postgres -h db-service test

```
