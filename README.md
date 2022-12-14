# [bamboo](#bamboo)

Ansible Role for Atlassian Bamboo Installation

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-bamboo/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bamboo/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-bamboo/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-bamboo)|[![quality](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/buluma/bamboo)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/buluma/bamboo)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bamboo.svg)](https://github.com/buluma/ansible-role-bamboo/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-bamboo.svg)](https://github.com/buluma/ansible-role-bamboo/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-bamboo.svg)](https://github.com/buluma/ansible-role-bamboo/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  become: true

  roles:
    - role: buluma.bamboo
```

The machine needs to be prepared. In CI this is done using `molecule/default/prepare.yml`:
```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: buluma.bootstrap
    - role: buluma.core_dependencies
    - role: buluma.setuptools
    - role: buluma.openssl
```


## [Role Variables](#role-variables)

The default values for the variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for bamboo

# bamboo release.
bamboo_master_version: 9.0.0
bamboo_master_fqdn: ""
bamboo_master_https: False
bamboo_master_port: ""

bamboo_master_include_jdk: True
bamboo_master_openjdk_version: 1.8.0

bamboo_master_user: bamboo
bamboo_master_application_folder: "/opt/atlassian/bamboo"
bamboo_master_data_folder: "/var/atlassian/application-data/bamboo"
bamboo_master_jvm_memory: 1g
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-bamboo/blob/main/requirements.txt).

## [Status of used roles](#status-of-requirements)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-bootstrap)|
|[buluma.openssl](https://galaxy.ansible.com/buluma/openssl)|[![Build Status GitHub](https://github.com/buluma/ansible-role-openssl/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-openssl/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-openssl/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-openssl)|
|[buluma.core_dependencies](https://galaxy.ansible.com/buluma/core_dependencies)|[![Build Status GitHub](https://github.com/buluma/ansible-role-core_dependencies/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-core_dependencies/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-core_dependencies/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-core_dependencies)|
|[buluma.setuptools](https://galaxy.ansible.com/buluma/setuptools)|[![Build Status GitHub](https://github.com/buluma/ansible-role-setuptools/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-setuptools/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-setuptools/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-setuptools)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-bamboo/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|oraclelinux|all|
|el|7, 8|
|opensuse|all|
|fedora|36, 35|

The minimum version of Ansible required is 4.10, tests have been done to:

- The previous version.
- The current version.
- The development version.



If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-bamboo/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-bamboo/blob/master/CHANGELOG.md)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)
