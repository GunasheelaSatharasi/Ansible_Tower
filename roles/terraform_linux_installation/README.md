## Role: Terraform Installation On Linux:
This Ansible playbook provides a set of tasks to download, install, and verify the installation of Terraform.

### Prerequisites:
- Ansible should be installed on the control machine.
- Internet connectivity is required to download Terraform.

### Usage:
1. Update the variables in the playbook as per your requirements:
   - `terraform_url`: The URL to download the Terraform archive.
   - `terraform_archive_dest`: The destination path for the downloaded Terraform archive.
   - `terraform_home`: The installation directory for Terraform.
   - `environment_path`: The environment path to include Terraform.

### What This Role DO:
- Download Terraform from the provided URL.
- Unzip the Terraform archive and place it in the specified installation directory.
- Verify the Terraform installation by running terraform --version.
- Display the Terraform version information.