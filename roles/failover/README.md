Role Name
=========

failover

Description
=========

This role creates a failover cluster and joins both primary and secondary systems.

Requirements
------------

- AD Controller
- Domain admin credentials
- Systems already joined the domain, you can use (oatakan.windows_cluster.join_domain role)
- oatakan.windows_cluster.failover_common role already run on both primary and secondary nodes

Role Variables
--------------

- cluster_name: testcluster
- cluster_ip_address: '192.168.100.20/24' # optional, if not specified dynamic ip will be used
- dns_domain_name: example.com
- cluster_file_share_witness: '\\Path\{{ cluster_name }}'
- cluster_quorom_enabled: false
- first_node: false # this should be set to true on the primary node, and false on secondary nodes

Dependencies
------------


Example Playbook
----------------

    - hosts: servers
      roles:
         - failover

License
-------

MIT

Author Information
------------------

- [Orcun Atakan](https://github.com/oatakan/)