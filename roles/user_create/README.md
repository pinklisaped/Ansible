User create
=========

The role creates user.

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------

```
# Username
uusername: ansible, ansible as default

# User password
upassword: 1234, doesn`t have default

# Sudo permissions
usudo: True, True as default

# Ask sudo password
unopasswd: False, {{ usudo }} as default

# User shell
ushell: /bin/bash, bin/bash as default

# Public key path
upublic_key: ~/.ssh/id_rsa.pub, doesn`t have default
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: grafana, uusername: someuser, upassword: 1234, usudo: False, ushell: /bin/sh, upublic_key: ~/.ssh/id_rsa.pub }

License
-------

BSD

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
