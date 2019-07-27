# ap-u18devlaptop

Follow the following steps to setup a new developer laptop on a fresh Ubuntu 18.04 bionic server image.

1. Install git and Ansible on dev laptop
2. Clone this repository to dev laptop
3. cd into the newly cloned repo
4. setup devlaptop for passwordless sudo

```
sudo nano /etc/sudoers
add this to the bottom of the file
user ALL=(ALL) NOPASSWD: ALL
```
5. edit username: in host_vars/localhost.yml to match your username
6. Run playbook on local machine
```ansible-playbook -i 'localhost,' -c local devlaptopsetup.yml```