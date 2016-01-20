puppet-master Ansible playbook
------------------------

This playbook will install Puppet 3.8 and has been tested on Centos 7 and should also work on RHEL 7.

Actions
--------

Installs all puppet pre-requisites including the following.

* puppet-master (3.8)
* puppetdb (3,2)
* hiera (3)
* facter (3.1)
* r10k (2.1.1)
* git
* puppet-lint

Configure puppetmater
* with puppetdb via ssl (:8081)
* hieradata in /etc/puppet/environments
* r10k will sync hieradata

Installing
------------

	$ git clone https://github.com/asmodeus70/Ansible-Playbooks.git

Running
---------

Install  Puppet master on a node called 'puppet' 

	$ ansible-playbook -i hosts install.yaml


