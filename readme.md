## Provision Centos7 VMs

```
cd vagrant
vagrant up
```

## Create Kubernetes cluster

```
ansible-playbook -i hosts ~/dev/kube-cluster/create-cluster.yml
```

## Join worker nodes to cluster

```
ansible-playbook -i hosts ~/dev/kube-cluster/join-cluster.yml
```

## Taint and label selected cluster nodes

```
kubectl taint nodes <node> <key>=<value>:NoSchedule
kubectl label nodes <node> <key>=<value>
```

## Initialize cluster with required objects

```
ansible-playbook -i hosts ~/dev/kube-cluster/initialize-cluster.yml
```
