#Install roles from ansible-galay 
 ansible-galaxy install -fr roles/requirements.yml


#Build jitsi server
 ansible-playbook build_jitsi_server.yml 


#Build videobridge server 
 ansible-playbook build_videobridge_servers.yml 


#Build coturn server 
 ansible-playbook build_coturn_servers.yml 


#Build jibri server 
ansible-playbook build_jibri_server.yml

#Configure all servers 
ansible-playbook main.yml


#List out servers which are running on ap-south-1a AZ using dynamic inventory
ansible ap-south-1 --list-hosts


#Purge everything 
ansible-playbook  purge.yml


#Ansible-vault encrypt/decrypt secret before production deployment  
ansible-vault encrypt group_vars/coturn/vars.yml
