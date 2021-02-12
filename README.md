# Ansible Nagios-XI and NCPA
An Ansible role for setting up the Nagios monitoring server and clients on CentOS Machines 

I've only selected certain platform that I know %100 works on Centos 7.6

# Requirements
Centos 7.x  machines

# Installing Nagios XI Server
To be able to install Nagios XI Server, you can use either option to complete the installation

### 1-Bootstrapping 

Add the following code into userdata
```
#!/bin/bash
sudo yum install curl -y
sudo curl https://assets.nagios.com/downloads/nagiosxi/install.sh | sh
```
### 2- Using the playbook

A. clone this repository into your machine

``` git clone https://github.com/turanmehmet/Project-1-nagios-xi.git ```

B. Add your hostnames into inventory-nagios-xi/hosts

C. Run the following command

```ansible-playbook -i inventory-nagios-xi/hosts  install-nagios-xi.yml ```

# Installing Nagios Client (NCPA)
Before you run the playbook, we need to configure your inventory. We will do this with dynamic way 
Go to this file `dynamic-inventory/ec2.ini` and set up your settings based on the comments and then,

Go to AWS and create a role with the following credentials and paste them in the same file (ec2.ini). 

```
aws_access_key_id = AXXXXXXXXXXXXXX`
aws_secret_access_key = XXXXXXXXXXXXXXXXXXX`
```
Run `install-ncpa.yml` playbook to install the nagios on the client machines


# Role information
install-nagios-xi role will install nagios xi monitor application on the desired machine.

install-ncpa role gives you the ability to install client of nagios-xi to monitor the resources.

# License
MIT

# Author Information

This role was created by [Mehmet Turan](https://github.com/turanmehmet).
