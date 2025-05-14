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

## Versioning

In order to have a versioning in place and working, create lightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag v2
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d v2
git push origin :refs/tags/v2
git tag v2
git push --tags
```
