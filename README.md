# Docs
Please read the official documentation.
https://vitastor.io/en/index.html#/
Ansible playbook for simple install from packages vitastor SDS on Ubuntu 22.04. 
## Project Structure
 - config/vitastor.conf.j2 - Conf file from vitastor MON daemon
 - playbook/install_vitastor.yml - ansible playbook for installation vitastor packages 
 - playbook/prepare_mon.yml - ansible playbook for prepare Monitor daemon and ETCD
 - playbook/prepare_osd.yml - ansible playbook for prepare disks and start OSD
 - var/main - Variables for playbook
 - inventory_example.ini - Inventory file
 ## Requirements
 - python => 3.10
 - ansible-core => 2.16

 ## Getting Started
 Check python version
 ```
 python3 -V
 ```
 If the command returns an error, you need to install python. 
 ```
 sudo apt update
 sudo apt install python3
 ``` 
 You can install ansible use pip.

 ```
 sudo apt install python3-pip
 sudo python3 -m pip install ansible-core
 ```
 Or instal use apt

 ```
 sudo apt update
 sudo apt install software-properties-common
 sudo add-apt-repository --yes --update ppa:ansible/ansible
 sudo apt install ansible
 ```
 Read the Docs https://vitastor.io/en/docs/intro/quickstart.html
## Prepare playbook
Specify the ip addresses for the monitors(ETCD) in the file /var/main and osd network
This network use from connect OSDs. If you need a separate network see oficial docs https://vitastor.io/docs/config/network.html#osd_cluster_network
In playbook prepare_osd you need listing storage disks in format /dev/sdXXX /dev/sdYYYY
See more information https://vitastor.io/en/docs/usage/disk.html
## Run playbook
