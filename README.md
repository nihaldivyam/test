# Divyam Azad

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

This repositiry enables to automate Docker deployment , Kubernetes deployment and Linux os hardening on the desired host files .
  - Tested on  
  - Ubuntu 18.0
  - Centos 8

#  Features!

  - One click full fledge deployment and os hardening
  
### Installation

It requires [Ansible 19.0 + ](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) to run.

Install the dependencies and start the ansibel 

```sh
$ ansible all -m ping # To check connectivity with all the hosts .
$ anible-playbook initial.yml # To start the initial process like adding user in all the servers . 
$ ansible-playbook docker.yml  # To install docker on all the specified machines .
$ ansible-playbook -i khosts kubernetes.yml  # To install kubernetes 
```

For Server Hardening 

# download and install Inspec
```sh
$ wget https://packages.chef.io/files/stable/inspec/4.20.2/ubuntu/20.04/inspec_4.20.2-1_amd64.deb
$ sudo dpkg -i inspec_4.20.2-1_amd64.deb
```

```sh
$ cd linux-harden
$ inspec exec linux-baseline
$ ansible-playbook  /linusx-harden/ansible-os-hardening.yaml
```
