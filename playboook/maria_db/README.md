# Ansible Playbook for Installing MariaDB:

- This playbook installs MariaDB on Linux hosts using Ansible. It supports Ubuntu, SUSE, and Red Hat distributions.

## Requirements
- This playbook requires Ansible to be installed on the system where the playbook will be executed.

## Usage
- To use this playbook, follow the steps below:

>1. Clone this repository to your local system
>2. Edit the dynamic-inventory file and the group_vars/main.yml file to customize the installation parameters as per your requirements.
>3. Run the playbook using the command ansible-playbook -i dynamic-inventory playbook.yml.

## Playbook Structure:

The playbook is structured as follows:

>1. Pre-tasks: These tasks update the repository indexes based on the Linux distribution. This ensures that the package manager has the latest package information before installation.

>2. Roles: The playbook includes a role named `maria_db`. This role contains the tasks required to install MariaDB, create the MySQL data directory, copy the installation script, start the MariaDB service, and secure the installation.

- The role can be found in the `roles/maria_db` directory relative to the playbook.

- If needed, you can modify the role or create additional roles to customize the MariaDB installation process.