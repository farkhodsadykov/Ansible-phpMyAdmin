# # Install phpMyAdmin with Ansible
This `ansible` playbook will install phpMyAdmin . Make sure you did all steps and then run playbook.  This playbook compatible with Centos/7

## Create digital-Ocean droplet with a token
1. Create  a token from digital Ocean [Craete token ](https://www.digitalocean.com/docs/api/create-personal-access-token/)
2. Create ssh-key and copy full path
3. Then run following commands

## AWS you can use ec2 instances
1. Create ec2 instance
2. ssh-copy to remote system
3. run the ansible playbook

```
git clone https://github.com/farkhodsadykov/Ansible-phpMyAdmin.git
cd Ansible-phpMyAdmin
vim hosts
# change the ipaddress
ansible-playbook -u root/ansible -i hosts install-mysql.yml
```

## Check the hosts is pining or not
```
ansible all -i hosts -u root -m ping
```
![](https://github.com/farkhodsadykov/Ansible-phpMyAdmin/blob/master/pictures/Screen%20Shot%202018-10-02%20at%209.33.04%20PM.png)


## Run the playbook
```
ansible-playbook -u root -i hosts install-mysql.yml
```
![](https://github.com/farkhodsadykov/Ansible-phpMyAdmin/blob/master/pictures/Screen%20Shot%202018-10-02%20at%209.30.56%20PM.png)

If you would like to change the password for MySQL,  go to `install-mysql.yml` change variable `new_passwd` to your new password. 😉
