# Ansible Nagios-XI
An Ansible role for setting up the Nagios monitoring server and clients on CentOS Machines 
I've only selected certain platform that I know %100 works on Centos 7.6

# Requrements
Centos 7.x client machines

# Installing Nagios XI Server
Two options
1- Add the following code into userdata
'''#!/bin/bash
sudo yum install curl -y
sudo curl https://assets.nagios.com/downloads/nagiosxi/install.sh | sh
'''
# Role information
install_ncpa role gives you the ability to install client of nagios-xi to monitor the resources.

# License
MIT

