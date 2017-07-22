# docker-compose

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-docker-compose.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-docker-compose)

ansible role to install Docker Compose.

https://galaxy.ansible.com/suzuki-shunsuke/docker-compose/

## Requirements

* Docker Engine

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
docker_compose_bin_dir: no | /usr/local/bin | | the directory path where the binary of docker-compose is installed
docker_compose_lib_dir: no | /usr/local/lib | | the directory path where the binary of docker-compose is installed
docker_compose_mode | no | 0755 | | the permission of the binary of docker-compose
docker_compose_version | yes | | 1.14.0 | docker-compose version

```
{docker_compose_lib_dir}/docker-compose-{docker_compose_version}  #  binary
{docker_compose_bin_dir|/docker-compose  # symbolic link
```

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.docker-compose
    docker_compose_version: 1.14.0
    become: yes
```

## License

[MIT](LICENSE)
