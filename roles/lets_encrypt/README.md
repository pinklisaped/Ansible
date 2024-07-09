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
lets_encrypt_site_dir: /var/www/html
lets_encrypt_acme_challenge_type: http-01
lets_encrypt_acme_challenge_dir: "{{ lets_encrypt_site_dir }}/.well-known/acme-challenge"
lets_encrypt_acme_dir: https://acme-v02.api.letsencrypt.org/directory
lets_encrypt_acme_version: 2
lets_encrypt_dir: /etc/letsencrypt
lets_encrypt_key_path: /etc/letsencrypt/keys
lets_encrypt_csr_path: /etc/letsencrypt/csrs
lets_encrypt_certs_dir: /etc/letsencrypt/certs
lets_encrypt_account_key_path: /etc/letsencrypt/accounts/account.key
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: lets_encrypt, lets_encrypt_acme_email: admin@somedomain.freemyip.com, domain_name: somedomain.freemyip.com }

License
-------

MIT

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
