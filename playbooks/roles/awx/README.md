# Ansible Role: awx

An Ansible role to deploy AWX by cloning the AWX repository and starting its services using Docker Compose.

## Requirements

- This role requires Ansible to be installed on the target machine.

## Role Variables

The following variables can be customized:

```yaml
# roles/awx/defaults/main.yml
```

# AWX Git repository URL
```yaml
awx_git_repo: https://github.com/ansible/awx.git
```

# Destination path for AWX repository clone
```yaml
awx_dest_path: /opt/awx
```

# Path to the Docker Compose file
```yaml
awx_compose_src: /opt/awx/installer/docker-compose.yml
awx_compose_dest: /opt/awx/docker-compose.yml
```

# Path to the AWX inventory file
```yaml
awx_inventory_dest: /opt/awx/installer/inventory
```

# Docker Compose environment variables
```yaml
awx_compose_env:
  - host_port: 80
  - pg_password: mysecretpassword
  - awx_official: true
  - project_data_dir: /var/lib/awx/projects
```

## Example Playbook
```
- hosts: awx_server
  roles:
    - awx
```

## License

This role is licensed under the MIT License. See the LICENSE file for details.

## Author Information
[gininfra](https://github.com/gininfra)
