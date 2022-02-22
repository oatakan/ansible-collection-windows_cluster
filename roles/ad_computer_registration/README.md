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

- role_action: register/unregister

Dependencies
------------



Example Playbook
----------------

    - hosts: servers
      roles:
         - ad_computer_registration

License
-------

MIT

Author Information
------------------

- [Orcun Atakan](https://github.com/oatakan/)