- To **upgrade** to new versions
- to secure **patches** for features to improve the efficiency
- **Installation** : to install certain application like Git and other required tools for development in all systems

Configuration management : was introduced for maintaining multiple servers.
Tools :
- Puppet
- Ansible 
- Chef
- Salt


Why ansible is used more?
 Puppet -> pull , master slave or master agent architecture ,Little bit difficult for window , codes should be puppet language
 Ansible -> push : from the laptop of developer and can push it to EC2 instance. Executing scripts from his laptop to all other and upgrade or whatever the thing to do regarding configuration 
 - Open source
 - Agentless architecture  : just put the DNS or IP address or names of the servers in a book called Inventory file, have password less authentication
 - Scaling up and down is made easy
 - Dynamic inventory : if new instances is created , it will take care of it with the others
 - have good modules for both Window and LINUX
 - It is simple : uses YAML language for scripting ,as it used in Kubernetes also
 - Developer can write his own Ansible modules
 - Ansible is written in Python
 - Using Ansible galaxy we can share modules
 - Supportive for enhancement and open source

Disadvantages of Ansible :
- slight problem in Windows for configuration management 
- Debugging issues 
- Little issues with performances

Ansible is developed by Red Hat.
Most of the organization is using ansible.

For installation go through Ansible documentation and I am working with ansible in EC2 instances

ansible playbook = ansible files
Inventory file : which stores the IP address of the target
Ansible adhoc commands:

For Practical look in scripts GitHub repo

Learn ANSIBLE dynamic inventory ? It is important