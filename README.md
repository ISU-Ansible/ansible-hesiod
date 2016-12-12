Hesiod
---------
[![Build Status](https://travis-ci.org/ISU-Ansible/ansible-hesiod.svg?branch=master)](https://travis-ci.org/ISU-Ansible/ansible-ssh)

The hesiod role is used to install Hesiod and the hesiod configuration file.

## Variables

### Global Variables
No global variables are used in this role.

### Role Variables
No role variables are used in this role.

### User Variables
No user-defined variables are used in this role.


## Tasks

### Description
This task fills out the template located in tempaltes/hesiod_conf.j2 to /etc/hesiod.conf on the selected system.

## Changed Files
- /etc/hesiod.conf

## Installed Programs
None. Hesiod is installed by default on RHEL systems.


## Example

### playbooks/hesiod.conf

    ---
    - name: Master Ansible Playbook
      hosts: all
      user: root
      connection: smart

      roles:
        - hesiod


### inventory/group_vars/all

    ---
    hesiod:
      lhs: ".ns"
      rhs: ".EXAMPLE.COM"
      classes: "HS,IN"
