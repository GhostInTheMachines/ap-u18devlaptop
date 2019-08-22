# ap-u18devlaptop

Follow the following steps to setup a new developer laptop on a fresh Ubuntu 18.04 bionic server image.

1. Install git
2. Install Ansible
```
sudo apt-get install software-properties-common \
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```
3. Clone this repository to dev laptop
4. cd into the newly cloned repo
5. setup devlaptop for passwordless sudo

```
sudo nano /etc/sudoers
add this to the bottom of the file
user ALL=(ALL) NOPASSWD: ALL
```
6. edit username: in host_vars/localhost.yml to match your username
7. Run playbook on local machine
```ansible-playbook -i 'localhost,' -c local devlaptopsetup.yml```
8. Log out of newly provisioned laptop and then log back in