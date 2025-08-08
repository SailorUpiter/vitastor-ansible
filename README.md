# Docs
Please read the official documentation.
https://vitastor.io/#/
Ansible playbook for simple install vitastor SDS on Ubuntu 22.04. 
## Project Structure
 - config/vitastor.conf - Conf file from vitastor MON daemon
 - playbook/install_vitastor.yml - ansible playbook for installation vitastor packages 
 - playbook/prepare_mon.yml - ansible playbook for prepare Monitor daemon and ETCD
 - playbook/prepare_osd.yml - ansible playbook for prepare disks and start OSD
 - inventory_example.ini - Inventory file
 ## Requirements
 - python => 3.10
 - ansible-core => 2.16

 ## Getting Started
 You can install ansible use pip.

 ```
 sudo apt install python3-pip
 ```

 ```
 sudo python3 -m pip install ansible-core
 ```
 Or
 
 ```
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```
