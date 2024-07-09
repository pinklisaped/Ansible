Grafana installation
=========

The role installs grafana.

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------

```
grafana_port: 3000
grafana_version: latest
ufw_allow_addr - not default, example 10.0.0.0/8
grafana_remove_repo: false - If your country doesn`t have access for https://apt.grafana.com/gpg.key use "true"
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: grafana, grafana_port: 3000, grafana_version: latest, ufw_allow_addr: any }

License
-------

MIT

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
