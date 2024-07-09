Self signed certificate
=========

Creates self signed certificate with TLSv3

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------

```
selfsign_certificate_ca_key: ca.key
selfsign_certificate_ca_path: ca.pem
selfsign_certificate_ca_passphrase: null
selfsign_certificate_key: cert-key.key
selfsign_certificate_path: certificate.key
selfsign_certificate_cn: "{{ ansible_host }}"
selfsign_certificate_san: "{{ selfsign_certificate_cn }}"
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: selfsign_certificate, selfsign_certificate_ca_key: /etc/keys/my-key.pem }

License
-------

MIT

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
