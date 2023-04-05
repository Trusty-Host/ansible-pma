**Note:** Needs for settings and install pma

Requirements
------------

- [x] Ansible version >= 2.14

Dependencies
------------
- [x] [ansible-common](https://github.com/Trusty-Host/ansible-common)
- [x] [ansible-nginx](https://github.com/Trusty-Host/ansible-nginx)
- [x] [ansible-php](https://github.com/Trusty-Host/ansible-php)
- [x] [ansible-mariadb](https://github.com/Trusty-Host/ansible-mariadb)

Installation
------------

- [x] git

Use `git@github.com:Trusty-Host/ansible-pma.git` to pull the latest edge commit of the role from git.

- [x] ansible-galaxy

Use `ansible-galaxy install -r requirements.yml` to install requirements roles

Platforms
---------

```yaml

Ubuntu:
  versions:
    - focal
    - bionic
```

Role Variables
--------------

The descriptions and default settings for all variables can be found in the **`defaults/main.yml`** directory in the following file:

- **[defaults/main.yml](./defaults/main.yml)**

## Example

### Configuration

```yaml
# Path to pma
pma_path: "/var/www/html/pma"
# Pma version
pma_version: 5.2.1
```


### Playbook

Use it in a playbook as follows:

```yaml
- hosts: all
  become: yes
  roles:
    - common
    - nginx
    - php
    - mariadb
    - pma
```

License
-------

[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
