# Create LXC containers using ansible
## To run containers building:
```sh
sudo ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory main.yml --extra-vars "ansible_user=containers_user password=containers_password"
```

ANSIBLE_HOST_KEY_CHECKING must be set to False because the host key for each building will be different. 

## To select containers to build use limit
Check inventory file to see available containers.

Available are ubuntu1, ubuntu2, ubuntu3
### Examples
Limit building to ubuntu1 and ubuntu3
```sh
sudo ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory main.yml --extra-vars "ansible_user=szymon password=test" --limit "ubuntu1,ubuntu3"
```
Limit building to ubuntu1
```sh
sudo ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory main.yml --extra-vars "ansible_user=szymon password=test" --limit "ubuntu1"
```