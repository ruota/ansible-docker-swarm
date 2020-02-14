# Ansible Docker Swarm

This project creates 2 CentOS VM throgh Vagrant and install ansible and docker on them,
the docker daemon API REST are protected with certificates and the docker partition is >= 40 GB.

Start a docker swarm manager on the local machine and 2 docker swarm nodes on the VMs and next
deploy an example service to docker swarm manager to test it.

Travis CI is implemented to check ansible syntax

## Getting Started


### Prerequisites

You Need Ansible >= 2.4

```
sudo apt install vagrant docker.io ansible
vagrant plugin install vagrant-disksize
vagrant plugin install vagrant-serverspec
```

### Installing

This is a simple ansible playbook run

```
ansible-playbook main.yml --extra-vars "ansible_sudo_pass=XXX"
```


