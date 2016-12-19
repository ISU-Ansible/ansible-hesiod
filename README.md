Hesiod
======
[![Build Status](https://travis-ci.org/ISU-Ansible/ansible-hesiod.svg?branch=master)](https://travis-ci.org/ISU-Ansible/ansible-hesiod)

The hesiod role is used to install and configure the Hesiod name service.


Requirements
------------
* Enterprise Linux 6
* Enterprise Linux 7

Role Variables
--------------
Defaults are:

    hesiod:
      rhs: ".EXAMPLE.COM"
      lhs: ".ns"
      classes: "HS,IN"

Dependencies
------------
No dependencies.

Example Playbook
----------------
To use the hesiod playbook, simply call it with your preferred variables.

    - hosts: servers
      vars:
        hesiod:
          rhs: ".MY.DOMAIN"
          lhs: ".ns"
          classes: "HS,IN"
      roles:
         - ISU-Ansible.hesiod

License
-------
GPL2

Author Information
------------------
* [Barry Britt (bbritt@iastate.edu)](bbritt@iastate.edu)
* [John Dickerson (jedicker@iastate.edu)](jedicker@iastate.edu)
