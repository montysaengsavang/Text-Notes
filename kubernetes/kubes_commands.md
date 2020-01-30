# Kubes Commands

## Get all pods in kubes cluster in dev namespace
`kubectl -n dev get po`

## Get pods in a kubes cluster filtered by keyword
`kubectl -n dev get po | grep [keyword]`

## Get logs from a pod
`kubectl logs -f [pod-name] -n dev`

## Get logs from a pod with multiple containers
`kubectl logs -f [pod-name] -n dev -c [container-name]`

## Get into an alpine container within a pod
`kubectl exec -it [pod-name] -n dev -c [container-name] /bin/ash`

## Get into a bash container within a pod
`kubectl exec -it [pod-name] -n dev -c [container-name] /bin/bash`

## Get verbose information on a specific pod
`kubectl describe pod [pod-name] -n dev`

## Get a list of all deployments in a kubes cluster
`kubectl -n dev get deployments`

## Get ingress urls of all pods
`kubectl -n dev get ingress`
