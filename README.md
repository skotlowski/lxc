# lxc
ansible and lxc learning

To run containers building:
sudo ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory main.yml --extra-vars "ansible_user=szymon ansible_password=test ansible_sudo_pass=test"
