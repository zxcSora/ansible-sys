Role Name
=========

This role control packages that should be on host and that should not.  
It suports many system version and controls with *sys_pkgs_present* variable.


* In case of debian 10 actual values will be from variable *sys_pkgs_10_present* 
```
sys_pkgs_present: "{{ lookup('vars', 'sys_pkgs_' + ansible_distribution_major_version + '_present')}}"
```

*  You can customise in any level of abstruction.
  - override *sys_pkgs_present*
  - override for selected os version *sys_pkgs_10_present*
  - override default packages for all systems *sys_pkgs_any_present:*
  - or just append list with your own

```
sys_pkgs_present: 
  - "{{ lookup('vars', 'sys_pkgs_' + ansible_distribution_major_version + '_present')}}"
  - "cowpatty"
```

* If your are pedant and want to control every version on target system or perform upgrade use prescise package definition

```
...
    - "base-files=9.9+deb9u11"
...
```

* same for package remove

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
