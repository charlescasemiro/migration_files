# migration\_files

Automation scripts designed to facilitate the migration of RHEL (Red Hat Enterprise Linux) servers using Ansible.

## Overview

This project provides Ansible playbooks and roles to automate the migration process of RHEL servers. It aims to streamline tasks such as configuration management, package installation, and system updates during server migration.

## Repository Structure

* `inventory.yml`: Defines the inventory of target hosts for Ansible.
* `main.yml`: The primary playbook that orchestrates the migration tasks.
* `roles/`: Contains Ansible roles used in the migration process.

  * `common/`: A role that includes common tasks applicable to all servers.

    * `tasks/`: Directory containing task files for the `common` role.

## Prerequisites

* Ansible installed on the control node.
* SSH access to the target RHEL servers.
* Properly configured `inventory.yml` with the target hosts.

## Getting Started

1. **Clone the Repository**

   ```bash
   git clone https://github.com/charlescasemiro/migration_files.git
   cd migration_files
   ```

2. **Configure the Inventory**

   Edit the `inventory.yml` file to include the target RHEL servers.

3. **Run the Playbook**

   Execute the main playbook using Ansible:

   ```bash
   ansible-playbook -i inventory.yml main.yml
   ```

   This command will initiate the migration tasks defined in the playbook.

## Customization

* Modify the `roles/common/tasks/` files to tailor the migration tasks to your specific requirements.
* Add additional roles as needed to handle specialized migration scenarios.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
