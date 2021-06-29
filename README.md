Notes:

Launching EC2 Instance:
============================
Create a IAM user.
Assign the EC2 full access policy.
Install Ansible on your server and python-pip.(ansible --version , Config file : /etc/ansible/ansible.cfg)
install Boto on the server(pip install boto)
Add the access key and Secret access with permission 400 under .boto 0r can provide directly in Playbook

To run the ansible-playbook Provision_Ec2.yml

For High available (HA):
Multiple instances/multiple availability zones.
EC2 instance to be deployed into an Auto Scaling (AS) group which will be linked to an Elastic Load Balancer (ELB).

============================================================================================================
Install docker compose
Give the permission chmode +X<path/docker-compose>
Create a docker-compose.yml for wordpress
Create a inventory file  and give the details of the managed nodes.(IP, username and password)
create configuration file and add the location of the inventory file on configutaion file.[/etc/ansible/ansible.cfg]
[default]
inventory = <path of inventoryfile>
ansible_host_key_checking=FALSE
We can check the Connectivity using the ping module:
ansible managed_node1 -m ping

To run the docker-compose.yml 
#docker-compose up




