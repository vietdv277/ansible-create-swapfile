# ansible-create-swapfile

# Ansible playbook to create swapfile on CentOS 7
1. Add ip address and root password of hosts in "hosts" file

[swapfile-hosts]
<ip_host>   ansible_ssh_user=root   ansible_ssh_pass='root_password_host'

2. Set swapfie size (MB) in group_vars/production
Example:

	---


	swapfile:
    	    size: '2048'

3. Run playbook

ansible-playbook -v main.yml
