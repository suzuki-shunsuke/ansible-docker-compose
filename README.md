docker-compose
===============

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-docker-compose.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-docker-compose)

Install Docker Compose.

https://galaxy.ansible.com/suzuki-shunsuke/docker-compose/

Requirements
------------

* Docker Engine

Role Variables
--------------

* docker_compose_nonroot: Whether the remote_user is root or not. This variable is set automatically, and is used to execute tasks with the become option.

Dependencies
------------

Nothing.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
  - { role: suzuki-shunsuke.docker-compose }
```

License
-------

MIT
