## Terraform On Linux Playbook:
This Ansible playbook installs Terraform on the target hosts.

### Prerequisites:
Before running this playbook, ensure that you have the following:
- Ansible installed on the control machine.
- Access to the target hosts via SSH.

### Usage:
- To use this playbook, follow the steps below:

>1. Clone this repository to your local system
>2. Edit the dynamic-inventory file and the group_vars/main.yml file to customize the installation parameters as per your requirements.
>3. Run the playbook using the command ansible-playbook -i dynamic-inventory playbook.yml.

### Variables:
1. Update the playbook variables:
   - `./group_vars/main.yml`: Update this file with the necessary variables for Terraform installation. Make sure to provide the correct values for variables like `terraform_version`, `terraform_download_url`, etc.
2. Ensure that the necessary roles are present:
   - `../../roles/tomcat_basic_packages_installation`: This role installs the required packages for Tomcat. Adjust the role path if needed.
   - `../../roles/terraform_installation`: This role installs Terraform. Adjust the role path if needed.
3. Update the playbook to specify the target hosts:
   - `hosts: tag_ansible_linux`: Replace `tag_ansible_linux` with the appropriate inventory group or host pattern that represents the target hosts.
4. After running the playbook, Terraform will be installed on the target hosts.