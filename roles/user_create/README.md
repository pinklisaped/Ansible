User create
=========

The role creates user.

Requirements
------------

- Rocky 9
- Ubuntu 20.04
- Ubuntu 22.04
- Ubuntu 24.04

Role Variables
--------------

```
# Username
user_create_name: ansible, ansible as default

# User password
user_create_password: 1234, doesn`t have default

# Sudo permissions
user_create_sudo: True, True as default

# Ask sudo password
user_create_sudo_nopasswd: False, {{ user_create_sudo }} as default

# User shell
user_create_shell: /bin/bash, bin/bash as default

# Public key path
user_create_public_key: ~/.ssh/id_rsa.pub, doesn`t have default
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: grafana, user_create_name: someuser, user_create_password: 1234, user_create_sudo: False, user_create_shell: /bin/sh, user_create_public_key: ~/.ssh/id_rsa.pub }

License
-------

BSD

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
