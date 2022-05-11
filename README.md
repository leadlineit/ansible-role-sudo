# Ansible Role Sudo

![Build Status](https://github.com/leadlineit/ansible-role-sudo/actions/workflows/ansible-galaxy-ci.yml/badge.svg)
[![Galaxy Role](https://img.shields.io/badge/Ansible--Galaxy-leadlineit.sudo-blue.svg?logo=ansible&logoColor=white)](https://galaxy.ansible.com/leadlineit/sudo/)

This role helps to install and configure sudo package on a Debian (stretch/buster/bullseye).

Requirements
------------

This role requires Ansible 2.5 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

```yaml
---
sudo:
  - file: root
    users:
      - your_user
    groups:
      - your_group
    command: ALL=(ALL) NOPASSWD:ALL
  - file: users
    users:
      - your_user
    groups:
      - your_group
    command: ALL=(ALL) ALL:ALL
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - { role: leadlineit.sudo, tags: sudo }
```

License
-------

BSD

Author Information
------------------

This role was created by Stas Stavnichuk.
