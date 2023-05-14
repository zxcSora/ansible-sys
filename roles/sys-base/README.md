Role Name
=========

Base debian system configuration.

* Why i should use this roles against raw modules?

Becouse it is centralized solution with good architecture struct and ability make own extensions and templates. 

* Most of default configuration make minimal influence on system. Make your own playbook.

* <var>_set - if you set to "no" this section will compleatly ignore

* timesyncd 

Conflicting with NTPD, so preferred way is to use timesyncd without rollback. 
In case of NTPD you shoud use separate role to make proper installation.
But NTPD is one of the main reason of botnet and  ddos. Think twice about.

* journald - preferred way on most system without rsyslog, options will be future releases.

* Swap - yes you can CRUD swap as you wish with just yaml.

* **sys_base_mount_by_path** works with uuid fstab records by default override **sys_base_mount_by_path_regex** as in default example if needed.

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
