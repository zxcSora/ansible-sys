### sys-net example
```
- name: configure client
  hosts: letyagin-ipsec-client-1
  become: true
  gather_facts: true
  roles:
    - role: "../roles/linux_networking"
      network:
        support:
          vlan: false
          bridge: false
          bonding: false
          traffic_forwarding: true
          ipv6: false

        purge_orphaned_interfaces: true
          
        interfaces:  # for more config-details see: https://wiki.debian.org/NetworkConfiguration
          eth0:
            address: '10.10.10.159/23'
            gateway: '10.10.10.1'
            aliases:
              - address: '192.168.88.101/24'
```