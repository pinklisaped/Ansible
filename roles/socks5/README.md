Socks5 server install
=========
The role set up socks5 proxy server

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------
```
socks5_port: 1080
socks5_loglevel: connect error
socks5_log_dir: /var/log/danted
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: socks5, socks5_port: 1234 }

License
-------

MIT

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
