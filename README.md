# ansible_nginx_vagrant_test

A simple web application hosted on a virtual machine with basic authentication automated using ansible, vagrant, and virtualbox.

This repository contains:
- Vagrantfile to spin up a Ubuntu 18.04 provisioned using `ansible`
- Ansible playbook code to configure packages and setup a reverse `nginx` proxy

To create and start configuring the guest machine do,

`vagrant up`

To SSH into the running vagrant machine & get shell access do,

`vagrant ssh`

To stop the running vagrant machine and destroy all resources do,

`vagrant destroy`

The vagrant machine is running a web server listening on port 80, with a forward port mapping to port 4444 on the host machine. `vagrant up` and connect to the application by hitting http://localhost:4444 on the host machine's browser.
