# nagios-xi
An Ansible role to install NCPA client of NagiosXI. 
I've only selected certain platform that I know %100 works on Centos 7.6

#Requrements
Centos 7.x client machines on AWS

#installing nagios xi
#!/bin/bash
sudo yum install curl -y
sudo curl https://assets.nagios.com/downloads/nagiosxi/install.sh | sh

#Role information
install_ncpa role gives you the ability to install client of nagios-xi to monitor the resources.

#License
MIT

