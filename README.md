Hesiod
---------
The hesiod role is used to install the default ISU Hesiod configuration file.

**NOTE**: This role is typically unnecessary in the standard ISU deployment. It is included only because some people still use Hesiod for lookups. We recommend using **sssd** or **ldap** for AD lookups.

**NOTE**: This role has been deprecated in favor of **sssd** and **ldap** for lookups.

## Variables

### Global Variables
No global variables are used in this role.

### Role Variables
No role variables are used in this role.

### User Variables
No user-defined variables are used in this role.


## Tasks

### Description
This task copies the file located in files/hesiod.conf to /etc/hesiod.conf on the selected system.

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
No variables are required for this role.
