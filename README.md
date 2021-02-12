# Ansible Nagios-XI
An Ansible role for setting up the Nagios monitoring server and clients on CentOS Machines 

I've only selected certain platform that I know %100 works on Centos 7.6

# Requrements
Centos 7.x client machines

# Installing Nagios XI Server
To be able to install Nagios XI Server, you can use either option to complete the installation

### 1-Bootstrapping 

Add the following code into userdata
```#!/bin/bash
sudo yum install curl -y
sudo curl https://assets.nagios.com/downloads/nagiosxi/install.sh | sh
```
### 2- Using the playbook

A. clone this repository into your machine

``` git clone https://github.com/turanmehmet/Project-1-nagios-xi.git ```

B. Add your hostnames into inventory-nagios-xi/hosts

C. Run the following command

```ansible-playbook -i inventory-nagios-xi/hosts  install-nagios-xi.yml ```

# Role information
install_ncpa role gives you the ability to install client of nagios-xi to monitor the resources.

# License
MIT

