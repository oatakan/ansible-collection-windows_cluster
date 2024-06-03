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

- join_domain_dns_domain_name: example.com
- join_domain_join_ou_path: '' # this is optional when joining to a specific ou path structure

Dependencies
------------


Example Playbook
----------------

```yaml
---
- name: join domain
  hosts: servers
  roles:
     - join_domain
```

License
-------

MIT

Author Information
------------------

- [Orcun Atakan](https://github.com/oatakan/)