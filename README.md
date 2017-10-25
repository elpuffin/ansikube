# ansikube

Ansible playbooks to install Kubernetes from upstream YUM repos. It uses kubeadm (beta) to do the initial instants and setup.

## Getting there

git clone the project from the above link and then run the ansible-playbook command against the inventory file and the site.yml

### Prerequisites

* Centos 7
* Kubernetes 1.8.1
* Ansible 2.4 on Fedora 26


## Deployment

Modify the inventoy file according to the setup in question.
e.g. with 1 master and 4 workers

```
k8s-master1 ansible_ssh_host=192.168.124.32
k8s-worker1 ansible_ssh_host=192.168.124.236
k8s-worker2 ansible_ssh_host=192.168.124.192
k8s-worker3 ansible_ssh_host=192.168.124.232
k8s-worker4 ansible_ssh_host=192.168.124.118

[masters]
k8s-master1

[workers]
k8s-worker1
k8s-worker2
k8s-worker3
k8s-worker4
```

## Authors

* **Raúl Martínez Sánchez** - *Initial Work* - nostrum@tuta.io

## License

Any Free Software Foundation one

## Acknowledgements

Partially based on the work done in following article

https://www.linuxtechi.com/install-kubernetes-1-7-centos7-rhel7/
