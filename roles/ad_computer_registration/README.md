Role Name
=========

ad_computer_registration

Description
=========

This role register computer object with the Active Directory controller using domain admin credentials.


Requirements
------------

- AD Controller
- Domain admin credentials

Role Variables
--------------

- ad_computer_registration_role_action: register/unregister

Dependencies
------------



Example Playbook
----------------
```yaml
---
- name: register computer
  hosts: servers
  roles:
     - ad_computer_registration
```

License
-------

MIT

Author Information
------------------

- [Orcun Atakan](https://github.com/oatakan/)