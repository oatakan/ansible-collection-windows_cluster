# ansible-collection-windows_cluster
This collection contains example roles for setting up Windows failover clusters.

It includes the following roles:

  - ad_computer_registration
  - failover
  - failover_common
  - join_domain

## Usage

Install this collection locally:

    ansible-galaxy collection install oatakan.windows_cluster -p ./collections

Then you can use the roles from the collection in your playbooks:

    ---
    - hosts: all
      roles:
        - oatakan.windows_cluster.failover_common

    - hosts: primary_server
      roles:
        - role: oatakan.windows_cluster.failover
          first_node: true

    - hosts: secondary_server
      roles:
        - role: oatakan.windows_cluster.failover
          first_node: false
