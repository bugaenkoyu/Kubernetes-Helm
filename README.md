# Kubernetes Helm Home Task

1. I brought the machine up on GCP and configured:
   - Cloned Kubespray release repository;
   - Copied and edited inventory file;
   - Turned on MetalLB;
   - Ran execute container;
   - Started ansible-playbook;
   - Copied kubectl configuration file;
   - Installed Ingress-controller.

How to do it in more detail is indicated in the repository [Deploy K8s with help Kubespray and ansible playbook](https://github.com/bugaenkoyu/k8s-with-kubespray-and-ansible).


2. The next step was to install Helm in the Kubernetes cluster.

I did next steps for it:

~~~
wget https://get.helm.sh/helm-v3.11.1-linux-amd64.tar.gz
tar -zxvf helm-v3.11.1-linux-amd64.tar.gz
mv linux-amd64/helm /usr/local/bin/helm
helm version
helm list
rm -r helm-v3.7.2-linux-amd64.tar.gz linux-amd64
~~~

![get helm version](images/helm-version.png)

Then I created deployment service and ingress files for deploying nginx with helm.