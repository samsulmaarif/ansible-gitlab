# Install GitLab with Ansible

Rather than creating from scratch, i use [this community contributed packages](https://github.com/geerlingguy/ansible-role-gitlab) as a role for this playbook.

Make sure you have `ansible` installed yourself on your system, and clone this repository recursively:

```
git clone --recursive https://github.com/samsulmaarif/ansible-gitlab.git 
cd ansible-gitlab
```

create the host file, and add your own server IP address:

```
cp hosts{.example,}
vim hosts
```

Create your configuration in vars directory:

```
cp vars/main.yml{.example,}
vim vars/main.yml
```

Adjust the variable value [as you can read it here in detail](https://github.com/geerlingguy/ansible-role-gitlab/blob/master/README.md#role-variables).

Run your playbook:

```
ansible-playbook -i hosts main.yml
```
