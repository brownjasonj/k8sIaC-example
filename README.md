Creating a cluster of VMs with a Kubernetes cluster (as an alternative to Minikube and Docker Desktop)

> vagrant up

The master node is set to have the ip address 192.168.50.10.

Get the kubernetes master configuration details for the kubectl

> scp -r vagrant@192.168.50.10:/home/vagrant/.kube .

password for the vagrant user on the master node is 'vagrant'.
copy the resulting directory to you home

> cp -r .kube/ ~/
> kubectl get nodes

should return the nodes in the kubenettes cluster.

If the above doesn't work then you need to login to the master and copy the config to your local machine.

> vagrant ssh master
> less ~/.kube/confg

copy the content of this file to your local ~/.kube/config file.

install the kubernetes cluster ui (https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/)
