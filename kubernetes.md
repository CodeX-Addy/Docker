docs: https://kind.sigs.k8s.io/docs/user/quick-start/

https://raw.githubusercontent.com/kubernetes-sigs/kind/main/site/content/docs/user/kind-example-config.yaml

# commands:

## install kind
brew install kind

## create a single node cluster
kind create cluster --name my-first-kind
kubectl cluster-info --context kind-my-first-kind

## delete the cluster
kind delete cluster --name my-first-kind

## create a cluster with 1 control plane and 2 worker nodes
kind create cluster --name my-first-kind --config config.yaml

## list the clusters
kind get clusters

# switch the context

kubectl config use-context kind-first-cluster
