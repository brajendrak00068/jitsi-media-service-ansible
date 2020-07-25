## 1. Install roles from ansible-galay 
ansible-galaxy install -fr roles/requirements.yml


## 2.Build jitsi server
 ansible-playbook build_jitsi_server.yml 


## 3.Build videobridge server 
 ansible-playbook build_videobridge_servers.yml 


## 4.Build coturn server 
 ansible-playbook build_coturn_servers.yml 


## 5.Build jibri server 
ansible-playbook build_jibri_server.yml

## 6.Configure all servers 
ansible-playbook main.yml


## 7.List out servers which are running on ap-south-1a AZ using dynamic inventory
ansible ap-south-1 --list-hosts


## 8.Purge everything 
ansible-playbook  purge.yml


## 9.Ansible-vault encrypt/decrypt secret before production deployment  
ansible-vault encrypt group_vars/coturn/vars.yml
