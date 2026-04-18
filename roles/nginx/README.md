Nginx Role
==========

An Ansible role to install and configure Nginx from the official maintainer repositories. It supports specific version pinning, dynamic module management, rate limiting configurations, and automated UFW firewall integration.

Requirements
------------

- Ubuntu 22.04 or higer

Role Variables
--------------

### Basic Configuration
| Variable | Default | Description |
| :--- | :--- | :--- |
| `nginx_state` | `present` | State of the nginx package. |
| `nginx_version` | `latest` | Desired version. Use `latest` or specific strings (e.g., `1.24.0`). |
| `nginx_service_enable` | `true` | Whether to enable the nginx service on boot. |
| `nginx_service_state` | `started` | Desired service state (started/stopped). |
| `nginx_repo` | `http://nginx.org/...` | Official repository URL. |
| `nginx_key` | `https://nginx.org/...` | URL for the GPG signing key. |

### Packages & Modules
| Variable | Default | Description |
| :--- | :--- | :--- |
| `nginx_modules` | `['acme', 'geoip']` | List of Nginx modules to install (translated to `nginx-module-<name>`). |
| `nginx_extra_packages`| `[]` | Additional system packages to install alongside Nginx. |
| `nginx_packages` | *(computed)* | Final list of packages combining core and modules. |

### Module Specific Configs
| Variable | Default | Description |
| :--- | :--- | :--- |
| `nginx_acme_enable` | `true` | Enables support for ACME/SSL workflows. |
| `nginx_rate_limits_enable`| `true` | Global toggle for rate-limiting configurations. |
| `nginx_rate_limits_zones` | *(complex)* | Dictionary defining connection and request limit zones using YAML anchors. |

### Firewall (UFW)
| Variable | Default | Description |
| :--- | :--- | :--- |
| `nginx_firewall_manage` | `true` | Automatically manage UFW rules for Nginx. |
| `nginx_firewall_ports` | `[80, 443]` | List of ports to open in the firewall. |

Dependencies
------------

role: selfsign_certificate

Example Playbook
----------------

Standard installation with specific version and modules:

```yaml
- hosts: servers
  vars:
    nginx_version: "1.28.3"
    nginx_modules:
      - acme
      - geoip
    nginx_firewall_ports:
      - 443
  roles:
    - role: phoenix.nginx_role
```
License
-------

MIT

Author Information
------------------

[@pinklisaped](https://github.com/pinklisaped)
