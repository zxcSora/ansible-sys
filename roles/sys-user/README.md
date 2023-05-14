Role Name
=========

Role to control user, groups and ssh keys. By default disable root password, add ansible user with offline public key, and remove garbage provider users(mostly legacy from cloudinit) 

* You can control groups and gid (add/remove)
* Feature if user is absent it will kill user process too. ex- backconnection, screens and so on.
* Feature parameter - if user have no activity more than timeout it will be locked.

```
inactive_timeout: # In days, disabled by default
```

* Good idea to have 2 keys to have ability to rotate ansible keys. If you do not use ansible user just ignore it.  
  
First change key1 than add key1 to ssh-agent and than change key2 and put both keys to ssh-agent.

```
sys_user_ansible_pub1: "files/ssh_pubs/offline_ansible.pub"
sys_user_ansible_pub2: "files/ssh_pubs/andrey_kasyanov.pub"
```

Requirements
------------

no

Role Variables
--------------

defaults/main.yml

Dependencies
------------

no

Example Playbook
----------------

playbooks/

License
-------

GPLv3

Author Information
------------------

AKA Andrey Kasyanov
