# Ansible role [bamboo](https://galaxy.ansible.com/ui/standalone/roles/buluma/bamboo/documentation)

Ansible Role for Atlassian Bamboo Installation

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-bamboo/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bamboo/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bamboo.svg)](https://github.com/buluma/ansible-role-bamboo/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-bamboo.svg)](https://github.com/buluma/ansible-role-bamboo/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-bamboo.svg)](https://github.com/buluma/ansible-role-bamboo/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/bamboo)](https://galaxy.ansible.com/ui/standalone/roles/buluma/bamboo/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-bamboo/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true

  roles:
    - role: buluma.bamboo
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-bamboo/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
    - role: buluma.bootstrap
    - role: buluma.core_dependencies
    - role: buluma.setuptools
    - role: buluma.openssl
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-bamboo/blob/master/defaults/main.yml):

```yaml
---
# defaults file for bamboo

# bamboo release.
bamboo_master_version: "9.4.4"
bamboo_master_fqdn: ''
bamboo_master_https: false
bamboo_master_port: ''
bamboo_master_include_jdk: true
bamboo_master_openjdk_version: "1.8.0"
# bamboo_master_openjdk_version: 17
bamboo_master_user: bamboo
bamboo_master_application_folder: /opt/atlassian/bamboo
bamboo_master_data_folder: /var/atlassian/application-data/bamboo
bamboo_master_jvm_memory: 1g
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-bamboo/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.openssl](https://galaxy.ansible.com/buluma/openssl)|[![Ansible Molecule](https://github.com/buluma/ansible-role-openssl/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-openssl/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-openssl.svg)](https://github.com/shadowwalker/ansible-role-openssl)|
|[buluma.core_dependencies](https://galaxy.ansible.com/buluma/core_dependencies)|[![Ansible Molecule](https://github.com/buluma/ansible-role-core_dependencies/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-core_dependencies/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-core_dependencies.svg)](https://github.com/shadowwalker/ansible-role-core_dependencies)|
|[buluma.setuptools](https://galaxy.ansible.com/buluma/setuptools)|[![Ansible Molecule](https://github.com/buluma/ansible-role-setuptools/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-setuptools/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-setuptools.svg)](https://github.com/shadowwalker/ansible-role-setuptools)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-bamboo/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-bamboo/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-bamboo/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-bamboo/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)
