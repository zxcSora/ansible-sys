Role Name
=========

This role autoconfigure ssh access for ansible

* first it scans ports
* than tryes to get ssh access with bunch of private keys
* than tryes to brute-force password
* and at the end print report and set ansible variables
* by-default if nothing found it will use ssh-agent and autodetected port

Common cases:

* autoconfigure access on just created vps  

most provider setup only root password, or only predefined key and so on

* detect weak passwords
* dynamicly detect ssh port  

with automatically change port to random one it makes harder for old school admin to  
do manual dirty magic without access restriction

* it can help to setup very old hosts that was poweroffed and nobody knows relevant password
* it cat help to get access on somebody else host but it cat break the law in most countries  

by default search stops on first valid credential found  
most probable user and password should be on top of dicts

Requirements
------------

amd64 arch

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
