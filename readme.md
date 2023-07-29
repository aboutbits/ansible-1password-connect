# Ansible 1Password Connect Role

A role to install and configure 1Password Connect.

## Requirements

- Docker and Docker Compose

## Role Variables

- `server_port`: 1Password Connect API server port (Optional). 
- `credentials_file`: The name of the 1Password credentials file template file (Optional). This file is used to authenticate with 1Password.

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-1password-connect
      vars:
        server_port: 8080
        credentials_file: 1password_credentials.j2
```

## Versioning

In order to have a verioning in place and working, create leightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag v1
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d v1
git push origin :refs/tags/v1
git tag v1
git push --tags
```
