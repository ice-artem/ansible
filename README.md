ansible -i hosts.txt ALL -m ping

with anssible.cfg 

ansible ALL -m ping

ansible-inventory --list
ansible-inventory --graph


ansible all -m apt -a "name=apache2 state=absent" -b

all = inventory or servers list
-m = module
-a = atribute 
-b = become

Ad-Hoc commands:

ansible all -m ping
ansible all -m setup
ansible all -m shell -a "uptime"
ansible all -m copy -a "src=yourfile.txt dest=/home/user mode=777" -b
ansible all -m file -a "path=/home/yourefile.txt state=absent" -b
ansible all -m get_url -a "url=https://your_link dest=/home/user" -b
ansible all -m yum -a "name=stress state=latest" -b 
ansible all -m yum -a "name=stress state=removed" -b

connection test to site
ansible all -m uri -a "url=http://www.yoursite.net return_content=yes"

ansible all -m yum -a "name=httpd state=latest" -b
ansible all -m service -a "name=httpd state=strted enabled=yes" -b

ansible-doc -l
