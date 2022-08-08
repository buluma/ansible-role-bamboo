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
  tasks:
    - name: "Include buluma.bamboo"
      include_role:
        name: "buluma.bamboo"
```


## [Role Variables](#role-variables)

The default values for the variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for bamboo

# bamboo release.
bamboo_release: "8.2"

# bamboo version.
bamboo_version: "{{ _bamboo_version[bamboo_release] }}"

# owner and group for Bamboo.
bamboo_owner: "bamboo"
bamboo_group: "bamboo"

# bamboo home directory.
bamboo_home: "/var/atlassian/application-data/bamboo"

# bamboo installation directory.
bamboo_catalina: "/opt/atlassian/bamboo"

# JVM minimal and maximum memory usage.
bamboo_jvm_minimum_memory: "2048m"
bamboo_jvm_maximum_memory: "2048m"

# proxy and context path setup.
bamboo_catalina_connector_proxyname: ~
bamboo_catalina_connector_proxyport: ~
bamboo_catalina_connector_scheme: "http"
bamboo_catalina_connector_secure: "false"
bamboo_catalina_context_path: ~

# atlassian Support recommended JVM arguments.
bamboo_jvm_support_recommended_args: >-
  -Datlassian.plugins.enable.wait=300
  -XX:+UnlockExperimentalVMOptions
  -XX:+UseCGroupMemoryLimitForHeap
  -XX:MaxRAMFraction=1

# session timeout (in minutes).
bamboo_session_timeout: "120"
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-bamboo/blob/main/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-bamboo/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|ubuntu|all|
|oraclelinux|all|
|opensuse|all|
|debian|all|
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
