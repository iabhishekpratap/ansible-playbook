# Ansible Playbooks

## Overview
This repository contains Ansible playbooks for automating various tasks such as server configuration, application deployment, and infrastructure management.

## Prerequisites
Before using these playbooks, ensure that you have the following installed:
- Ansible (>=2.9)
- Python (>=3.6)
- SSH access to target machines
- Inventory file configured with the appropriate hosts

## Directory Structure
```
.
├── self-01.yml          # Custom playbook
├── self-02.yml          # Custom playbook
├── env.yml              # Environment variables
├── variable.yml         # Variable definitions
├── README.md            # Documentation
├── script/              # Scripts used in playbooks
├── tf-config/           # Terraform configuration files
├── 00-first-pb.yml      # First playbook
├── 01-app-install.yml   # Application installation
├── 02-copy-files.yml    # Copying files
├── 03-file-module.yml   # File module usage
├── 04-change-permission.yml # Changing file permissions
├── 05-script-run.yml    # Running scripts
├── 06-cron-job.yml      # Creating cron jobs
├── 07-cron-modify.yml   # Modifying cron jobs
├── 08-user-manage.yml   # User management
├── 09-set-pass.yml      # Setting user passwords
├── 10-download-file.yml # Downloading files
├── 11-kill-process.yml  # Killing processes
├── 12-firewall.yml      # Firewall configurations
├── 13-conditions.yml    # Conditional execution
```

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/iabhishekpratap/ansible-playbook.git
   cd ansible-playbook
   ```
2. Update the inventory file with target machine details.
3. Run a playbook using the following command:
   ```bash
   ansible-playbook <playbook-name>.yml
   ```

## Best Practices
- Use roles to structure your playbooks.
- Keep sensitive data in Ansible Vault.
- Use `ansible-lint` to maintain code quality.
- Test playbooks in a staging environment before applying to production.

## Troubleshooting
- To enable verbose mode for debugging, add `-vvv` to the command.
- Check `ansible.cfg` for configuration settings.
- Verify SSH connectivity using:
  ```bash
  ansible -i inventory/hosts.ini all -m ping
  ```

## License
This project is licensed under the MIT License.

## Contributors
Feel free to submit issues or pull requests to improve this repository.

