# Configuring Apache Web Server

This playbook is used to configure the Apache web server on Linux hosts. It installs and configures the Apache web server and sets up firewall rules to allow incoming HTTP traffic.

## Prerequisites
- Ansible installed on the control machine.
- SSH access to the target hosts.

## Usage
- To use this playbook, follow the steps below:

>1. Clone this repository to your local system
>2. Edit the dynamic-inventory file and the group_vars/main.yml file to customize the installation parameters as per your requirements.
>3. Run the playbook using the command ansible-playbook -i dynamic-inventory playbook.yml.

## Roles
This playbook uses the following Ansible roles:
- `apache_webserver`: Installs and configures the Apache web server.
- `firewalld`: Sets up firewall rules to allow incoming HTTP traffic.