# p1-learn-ansible1

Ansible Installation Steps:
----------------------------
yum list all | grep python
yum install python3.11-devel.x86_64D
yum install python3.11-pip.noarch
pip3.11 install ansible

Ansible Docs:
--------------
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/index.html#plugins-in-ansible-builtin

ansible.builtin commands(NGINX installation):
--------------------------------------------
ansible -i inv WEB -e ansible_user=centos -e  ansible_password=DevOps321 -b -m ansible.builtin.yum -a "name=nginx state=latest"

ansible.builtin commands(NGINX service started):
------------------------------------------------
ansible -i inv WEB -e ansible_user=centos -e  ansible_password=DevOps321 -b -m ansible.builtin.systemd -a "name=nginx state=started"

