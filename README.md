# 1. Fix locale settings warning on Debian 9 (stretch) with [Ansible](https://www.ansible.com/)

1. Clone this repository locally:
```https://github.com/moovs/setting-locale-settings.git```
2. Add your ssh-key to the host when you want to fix warning:
```ssh-copy-id -i ~/.ssh/id_rsa.pub user@host```
- This logs into the server host, and copies keys to the server, and configures them to grant access by adding them to the authorized_keys file.
3. Just set up your server's IP in hosts file for example:
``` 
[my_group]
my_domain ansible_ssh_host=192.168.0.0 ansible_ssh_user=my_user
```
4. And run: 
```ansible-playbook -i hosts ./roles/locale/main.yml```
5. You have fixed locale settings warning on your host :alien:

***
### Author
[Nikolay Ovsiannikov](https://www.linkedin.com/in/nikolay-ovsiannikov/) - LinkedIn
