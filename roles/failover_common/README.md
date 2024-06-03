Role Name
=========

failover_common

Description
=========

This role implements prerequisite steps for a failover cluster on all nodes. It ensures that necessary features and
services are installed and configured to support a Windows failover cluster.

Requirements
------------


Role Variables
--------------

See defaults/main.yml for a list of variables used in this role.

Dependencies
------------


Example Playbook
----------------
    
```yaml
---
- name: perform fail over common tasks on all systems
  hosts: servers
  roles:
     - failover_common
```

License
-------

MIT

Author Information
------------------

- [Orcun Atakan](https://github.com/oatakan/)