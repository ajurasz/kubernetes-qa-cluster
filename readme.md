## Create Kubernetes cluster

```
ansible-playbook -i hosts ~/dev/kube-cluster/create-cluster.yml
```

## Join worker nodes to cluster

```
ansible-playbook -i hosts ~/dev/kube-cluster/join-cluster.yml
```

## Initialize cluster with required objects

```
ansible-playbook -i hosts ~/dev/kube-cluster/initialize-cluster.yml
```
