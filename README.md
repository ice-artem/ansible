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


