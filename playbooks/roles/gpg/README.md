# Ansible Role: docker

An Ansible role to install Docker and Docker Compose dependencies using DNF and the geerlingguy.docker role.

## Requirements

- This role requires Ansible to be installed on the target machine.

## Role Variables

The following variables can be customized:

```yaml
# roles/docker/defaults/main.yml

# List of packages to be installed with DNF
```
docker_dnf_deps:
  - python3-pip
  - python3-setuptools
```

# Name of the geerlingguy.docker Ansible Galaxy role
```
docker_geerlingguy_docker_role: geerlingguy.docker
```

## Dependencies
```
    geerlingguy.docker role: geerlingguy.docker
```

## Example Playbook

```yaml
- hosts: all
  roles:
    - docker
```

## License

This role is licensed under the MIT License. See the LICENSE file for details.

## Author Information
[gininfra](https://github.com/gininfra)

