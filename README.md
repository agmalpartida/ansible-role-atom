Ansible Role: Atom Packages
===========================

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/gantsign/ansible-role-atom/master/LICENSE)

Role to customize the [atom.io](https://atom.io) text editor by
GitHub.

Requirements
------------

* Ansible >= 2.7

Role Variables
--------------

The following variables will change the behavior of this role (default values
are shown below):

```yaml
# Users to install packages for
users: []
```

Users are configured as follows:

```yaml
users:
  - username: # Unix user name
    atom_packages:
      - # package 1
      - # package 2
```

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: agmalpartida.atom
      users:
        - username: vagrant
          atom_packages:
            - minimap
            - linter
            - atom-beautify
            - file-icons
```

License
-------

MIT
