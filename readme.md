# Ansible 1Password Connect Role

A role to install and configure 1Password Connect.

## Requirements

- Docker and Docker Compose

## Role Variables

- `onepassword_server_port`: 1Password Connect API server port (Optional). 
- `onepassword_credentials_file`: The name of the 1Password credentials file template file (Optional). This file is used to authenticate with 1Password.

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-1password-connect
      vars:
        onepassword_server_port: 8080
        onepassword_credentials_file: 1password_credentials.j2
```

## Build & Publish

To build and publish the role, visit the GitHub Actions page of the repository and trigger the workflow "Release Package" manually.
