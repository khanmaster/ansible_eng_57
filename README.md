### Run below commands to see the magic of Ansible
- Run these commands from Ansible controller to all Agent nodes or with specific name of the node.

```ansible
ansible all -m ping
ansible aws -m ping
ansible all -a "uname -a"

ansible all -a "date"
ansible all -a "free -a"
ansible all -a "free -a"
```
There are plenty more Ad-hoc commands available on Ansible
``` doc page
https://docs.ansible.com/ansible/latest/user_guide/intro_adhoc.html```
```


## install sql with playbook

```ansible

---
# installing Mysql on a server called db

- hosts: db
  become: true
  tasks:
  - name: Install mysql
    apt: pkg=mysql-server state=present
```