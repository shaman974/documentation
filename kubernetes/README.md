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

## Commande en vrac

### base

  kubectl cluster-info
  
  kubectl get nodes
  
  kubectl get ns
  
  kubectl create ns testns
  
### debug

créer un conteneur de debug

  kubectl run -it —rm —image=alpine debug