# Examples

## Deploy network policies

```shell

  kubectl apply -f ./k8s/network-policies/deployment

```

## Delete network policies

```shell

  kubectl delete -f ./k8s/network-policies/deployment

```

## How to connect to one of the postgres-clients

```shell

  kubectl exec good -n network-demo -it -- "/bin/sh"

```
