Ansible Cobalt Strike (Docker)
=========
[![CI](https://github.com/warhorse/ansible-role-neo4j-docker/workflows/CI/badge.svg?event=push)](https://github.com/warhorse/ansible-role-neo4j-docker/actions?query=workflow%3ACI)
[![warhorse.neo4j_docker](https://img.shields.io/ansible/role/55904)](https://galaxy.ansible.com/warhorse/neo4j_docker)
[![warhorse.neo4j_docker](https://img.shields.io/ansible/quality/55904)](https://galaxy.ansible.com/warhorse/neo4j_docker)
[![warhorse.neo4j_docker](https://img.shields.io/ansible/role/d/55904)](https://galaxy.ansible.com/warhorse/neo4j_docker)
![License](https://img.shields.io/github/license/warhorse/ansible-role-neo4j-docker)
![Commit](https://img.shields.io/github/last-commit/warhorse/ansible-role-neo4j-docker)

![Neo4j Logo](./images/neo4j_logo.png "Neo4j Logo")


Install Neo4j (Docker)

This role is part of the Warhorse Automation Framework. This role can be used with Warhorse or as a standalone role.

Docker Image
-------------

[docker-neo4j](https://github.com/neo4j/docker-neo4j)

Role Variables
--------------

A list of all the variables can be found in ./defaults/main.yml.

`neo4j_dir` - Neo4j container directory 

`neo4j_docker_version` - Docker image version

`neo4j_ports` - Neo4j container ports

`neo4j_hostname` - Neo4j container hostname

`neo4j_container_name` - neo4j container name 

`neo4j_username` - Neo4j username

`neo4j_password` - Neo4j password 

`neo4j_docker_network` neo4j container docker network


Dependencies
------------

```shell
ansible-galaxy install geerlingguy.docker geerlingguy.pip
```

Install
------------

```shell
ansible-galaxy install warhorse.neo4j_docker
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
      - { role: warhorse.neo4j_docker }
```

Example Vars
----------------

```yaml
neo4j_hostname: "neo4j"
neo4j_container_name: "neo4j"
neo4j_docker_version: "latest"
neo4j_username: "neo4j"
neo4j_password: "password"
neo4j_docker_labels: {}
neo4j_docker_network: "neo4j"
neo4j_dir: '/opt/docker/neo4j'
neo4j_ports:
  - "7474:7474"
  - "7687:7687"
```

License
-------

MIT/BSD

Author Information
------------------

Ralph May
