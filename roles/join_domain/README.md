Role Name
=========

join_domain

Description
=========

This role joins the system to a domain.

Requirements
------------

- AD Controller
- Domain admin credentials

Role Variables
--------------

- dns_domain_name: example.com
- join_ou_path: '' # this is optional when joining to a specific ou path structure

Dependencies
------------


Example Playbook
----------------

    - hosts: servers
      roles:
         - join_domain

License
-------

MIT

Author Information
------------------

- [Orcun Atakan](https://github.com/oatakan/)