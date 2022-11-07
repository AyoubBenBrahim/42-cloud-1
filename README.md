

python3 -m pip install --user ansible

vim ~/.zshrc

export PATH="$HOME/Library/Python/3.7/bin:$PATH"

ansible-vault encrypt inception/.env

ansible-playbook -i inventory.ini main_playbook.yaml --ask-vault-pass



wordpress ==> https://192.168.42.20
phpMyAdmin ==> https://192.168.42.20:8080



python3 -m pip install requests
python3 -m ensurepip --upgrade
python3 -m pip install --upgrade pip
python3 -m pip install --user ansible



ansible-inventory -i inventory.ini --list
ansible all -i inventory.ini -m ping


#single task
ansible-playbook -i inventory.ini main_playbook.yaml --tags=start_mariadb --ask-vault-pass

 ansible-playbook main_playbook.yaml --tags=rm_all --extra-vars "confirmation=yes" --ask-vault-pass

confirmation default value = no

 Variables passed during playbook runtime take the highest precedence and override the variables defined in the playbook. 
 https://www.cherryservers.com/blog/how-to-use-variables-in-ansible-playbooks

 ansible-playbook main_playbook.yaml --tags=start_mariadb --extra-vars "srv=yes confirmation=yes" --ask-vault-pass