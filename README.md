[![CircleCI](https://circleci.com/gh/ansible-roles-mamono210/docker/tree/main.svg?style=svg)](https://circleci.com/gh/ansible-roles-mamono210/docker/tree/main)

Role Description
=========

Installs Docker for Linux.

Requirements
------------

None

Role Variables
--------------

```YAML
---
docker_edition: 'ce'
docker_packages:
  - "docker-{{ docker_edition }}"
docker_packages_state: present


docker_yum_repo_url: https://download.docker.com/linux/centos/docker-ce.repo
docker_yum_repo_enable_nightly: '0'
docker_yum_repo_enable_test: '0'
docker_yum_gpg_key: https://download.docker.com/linux/centos/gpg
```

Dependencies
------------

None

Example Playbook
----------------

```YAML
---
- hosts: all
  become: true
  roles:
    - role: docker
```

License
-------

BSD
