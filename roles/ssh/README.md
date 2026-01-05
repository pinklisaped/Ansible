SSH config
=========

Role configures ssh server
The role can change ssh port and save new port in ssh config for local user.
As well it add antiscan-shield. When anynyone scans 22 port, ufw blocs him on `ssh_fwd_bantime` time for all ports. Behavour disabled if `ssh_port` is 22.

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
------------
```
# Vars for ssh.conf
ssh_ignore_rhosts: true
ssh_password_authentication: false
ssh_permit_root_login: false
ssh_disable_forwarding: true
ssh_port: random # Changes the default value for another persistent port
ssh_fwd_bantime: 86400 # Secs 86400 - 1 day, 604800 - 7 days
ssh_save_host: true # Saves this host in ssh conf
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