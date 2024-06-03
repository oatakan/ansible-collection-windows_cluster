# Ansible Collection: oatakan.windows_cluster

This Ansible collection provides roles to manage Windows failover clusters. It includes four primary roles designed to simplify the process of setting up and managing Windows clusters, which are:

1. `ad_computer_registration`: This role is used for registering computers in Active Directory (AD). For more information, refer to the role's documentation within its directory.

2. `failover`: This role creates a failover cluster and joins both primary and secondary systems. It requires an AD Controller, domain admin credentials, and the systems to be already joined to the domain. The `failover_common` role must have been run on all nodes before using this role. For more details, check out the `README.md` file in the role's directory.

3. `failover_common`: This role implements prerequisite steps for failover cluster for all nodes. It ensures that necessary features and services are installed and configured on your system to support a Windows failover cluster. Refer to its `README.md` for more information.

4. `join_domain`: This role is used for joining the system to a domain. It requires an AD Controller and domain admin credentials. To learn more about this role, refer to its `README.md`.

## Publishing to Ansible Galaxy

This section provides a guide on how to build and publish this collection to the Ansible Galaxy.

### Building the Collection

1. Navigate to the root directory of your local repository where `galaxy.yml` is located.
2. Run the following command to build the collection:
   ```shell
   ansible-galaxy collection build

### Publishing the Collection

1. Navigate to the root directory of your local repository where `galaxy.yml` is located.
2. Run the following command to publish the collection:
   ```shell
   ansible-galaxy collection publish oatakan-windows_cluster-1.0.0.tar.gz

## Usage

To use these roles in your Ansible playbooks, follow these steps:

1. Install the collection locally using the command:

    ansible-galaxy collection install oatakan.windows_cluster -p ./collections

2. Include the desired role in your playbook like this:
 ```yaml
 ---
 - name: setup windows cluster
   hosts: all
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
```
