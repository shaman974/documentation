# kubernetes

## Documentation

https://kubernetes.io

https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/

## Autre distribution

https://www.padok.fr/en/blog/minikube-kubeadm-kind-k3s

### K3S

https://rancher.com/docs/k3s/latest/en/installation/installation-requirements/

https://github.com/rancher/k3s/blob/master/docker-compose.yml

https://k3s.io

## Test local

https://k3d.io

https://github.com/rancher/k3d

creer un nouveau cluster

 k3d cluster create mycluster
 
 avec mapping du repository
 
  k3d cluster create mycluster --volume "/Users/rvetrano/workspace/perso/test-kube-commande/registries.yaml:/etc/rancher/k3s/registries.yaml"

avec mapping du ingress pour le developpeur et du volume

k3d cluster create mycluster --volume "/Users/rvetrano/workspace/perso/test-kube-commande/registries.yaml:/etc/rancher/k3s/registries.yaml" --api-port 6550 -p "8081:8079@loadbalancer" --agents 2


supprimer un cluster

k3d cluster delete mycluster

k3d cluster list

k3d cluster start mycluster

## Commande en vrac

https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands

https://kubernetes-snippets.com

### base

  kubectl cluster-info
  
  kubectl get nodes
  
  kubectl get ns
  
  kubectl create ns testns
  
  kubectl config set-context --current --namespace=testns
  
  kubectl delete pods commande-kube
  
  kubectl apply -f k3sFile.yml
  
  kubectl -n testns delete pod,svc,replicasets,deployments,ingress --all
  
  kubectl edit ingress test
  
  kubectl describe ingress myapp
  
### debug

voir ce qui c'est passé

kubectl describe pods <<nom du pod>>

kubectl describe pods commande-kube

kubectl logs -f commande-kube


créer un conteneur de debug

  kubectl run -it --rm --image=debian:9-slim debug
  apt-get update
  apt-get install curl
