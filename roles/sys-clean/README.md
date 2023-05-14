Role Name
=========

* Clean logs, history, caches
* Compleatly purge(zero block devices)
* By-default delete: 
  - "/etc/dhcp/dhclient.d/google_hostname.sh"
  - "/etc/dhcp/dhclient-exit-hooks.d/google_set_hostname"

Common cases is: 

* If you want prepare and give host to another owner.

```
sys_clean_apt: "yes"
sys_clean_history: "yes"
sys_clean_logs: "yes"
```

* If you want remove all your date on host with no easy way to recover. ex. Revert hw. server to provider. 

```
sys_clean_purge: "yes"
```
  
* If you are pedant and want your system be smooth and pretty.
```
sys_clean_apt: "yes"
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
