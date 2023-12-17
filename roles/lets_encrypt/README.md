Lets Encrypt receiver
=========
The role get let`s encrypt certificate

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------
```
domain_name: your-domain # Doesn`t have default
lets_encrypt_acme_email: certificate-reminders@your-domain # Doesn`t have default
lets_encrypt_site_directory: /var/www/html
lets_encrypt_acme_challenge_type: http-01
lets_encrypt_acme_challenge_directory: "{{ lets_encrypt_site_directory }}/.well-known/acme-challenge"
lets_encrypt_acme_directory: https://acme-v02.api.letsencrypt.org/directory
lets_encrypt_acme_version: 2
lets_encrypt_dir: /etc/letsencrypt
lets_encrypt_keys_dir: /etc/letsencrypt/keys
lets_encrypt_csrs_dir: /etc/letsencrypt/csrs
lets_encrypt_certs_dir: /etc/letsencrypt/certs
lets_encrypt_account_key: /etc/letsencrypt/account/account.key
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: lets_encrypt, lets_encrypt_acme_email: admin@somedomain.freemyip.com, domain_name: somedomain.freemyip.com }

License
-------

BSD

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
