IPSec installation
=========

The role installs and configures IPSec.

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------

```
ipsec_server_leftid: "{{ ansible_host }}"
ipsec_server_leftsubnet: 0.0.0.0/0
ipsec_server_rightsourceip: 10.0.0.0/24
ipsec_server_rightdns: 8.8.8.8,8.8.4.4
ipsec_server_compress: false
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ipsec_server, ipsec_server_leftid: "CN=somedomain.freemyip.com" }

License
-------

BSD

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
