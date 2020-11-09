# hobbyfarm

### Requirements

- [Vagrant](https://www.vagrantup.com)
- [VirtualBox](https://www.virtualbox.org)
- [Helm](https://helm.sh/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- 6GB unused RAM


The helm chart repo for hobbyfarm can be installed using:
helm repo

helm repo add hobbyfarm https://hobbyfarm.github.io/hobbyfarm

In order to obtain values for it, once installed

helm show values hobbyfarm/hobbyfarm > values.yml

Once customized it can be deployed using:

helm install -f values.yaml hobbyfarm/hobbyfarm --namespace hobbyfarm

It can be removed using:
helm uninstall hobbyfarm --namespace hobbyfarm

The namespace is a requirement of hobbyfarm current status.

Futher information for creating the k8s cluster with Rancher can be found in:
https://rancher.com/docs/rancher/v2.x/en/quick-start-guide/deployment/quickstart-vagrant/
