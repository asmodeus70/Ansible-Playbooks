puppet-master
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

	$ git clone git@github.com:daniellawrence/ansible-puppetmaster.git
	$ mkvirtualenv ansible
	$ pip install ansible

Running
---------

Install a puppetmaster on a node called 'puppet' (change the hosts.ini)

	$ ansible-playbook -i hosts.ini install.yaml


Testing
---------

The tests assume that you have ansible and docker installed on your
local machine.  By running `./tests/run_tests.sh` a new machine
will be created and ansible will take over and install the puppetmaster.

The `ubuntu:14.04` is also assumed to be installed locally.

Buildout
----------
serverspec will make sure that everything is install and configured as
it should be.
