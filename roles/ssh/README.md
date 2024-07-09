Role Name
=========

Role configures ssh server

Role Variables
------------
```
# Vars for ssh.conf
ssh_ignore_rhosts: true
ssh_password_authentication: false
ssh_permit_root_login: false
ssh_disable_forwarding: true

ssh_failban_maxretry: 5
ssh_failban_findtime: 60
ssh_failban_bantime: 600
ssh_failban_ignoreip: 127.0.0.1/8 10.0.0.0/8 192.0.0.0/8
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ssh, ssh_ignore_rhosts: true, ssh_password_authentication: false, ssh_permit_root_login: false, ssh_failban_maxretry: 5, ssh_failban_findtime: 60, ssh_failban_bantime: 600, ssh_failban_ignoreip: 127.0.0.1/8 }

License
-------

MIT

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)