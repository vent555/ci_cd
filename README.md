# Lab task: CI/CD with Jenkins and deployment in Kubernetes
## Install Jenkins
* Create VM using vagrant
* Configure VM with ansible
## Setup Kubernetes cluster
* Create VMs using vagrant
* Configure VMs with ansible
```sh
ansible-playbook -l kubernetes main.yml
```
### Create Kubernetes cluster with two nodes
* On node k8s1:
```sh
vagrant@k8s1:~$ microk8s add-node
```
* On node k8s2 (192.168.50.101:25000/_token_ get from output command "microk8s add-node" on node k8s1):
```sh
vagrant@k8s2:~$ microk8s join --skip-verify 192.168.50.101:25000/1557b3febe66615a26056898a48e41b6/867c35a86f2e
```
### Configure access from localhost to the created cluster
* Install kubectl utility
* On node k8s1:
```sh
vagrant@k8s1:~$ microk8s config
```
* Save output on the local machine in a file ~/.kube/config
* Verify configuration:
```sh
kubectl cluster-info
kubectl get nodes
```