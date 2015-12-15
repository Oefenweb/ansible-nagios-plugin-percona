## nagios-plugin-percona 

[![Build Status](https://travis-ci.org/Oefenweb/ansible-nagios-plugin-percona.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-nagios-plugin-percona) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-nagios-plugin-percona-blue.svg)](https://galaxy.ansible.com/list#/roles/6547)

Set up [Percona Monitoring Plugins](https://www.percona.com/software/mysql-tools/percona-monitoring-plugins) for Nagios in Debian-like systems

#### Requirements

None

#### Variables

* `nagios_plugin_percona_install`: [default: `[]`]: Additional packages to install

* `nagios_plugin_percona_my_cnf_files`: [default: `[]`]: `.my.cnf` files to configure
* `nagios_plugin_percona_my_cnf_files.{n}.dest`: [optional, default: `~owner/.my.cnf'`]: The remote path of the file to copy
* `nagios_plugin_percona_my_cnf_files.{n}.owner`: [required]: The name of the user that should own the file
* `nagios_plugin_percona_my_cnf_files.{n}.group`: [optional, default: `owner`]: The name of the group that should own the file
* `nagios_plugin_percona_my_cnf_files.{n}.mode`: [optional, default: `0600`]: The mode of the file
* `nagios_plugin_percona_my_cnf_files.{n}.login_host`: [optional, default: `localhost`]: The host running the server
* `nagios_plugin_percona_my_cnf_files.{n}.login_port`: [optional, default: `3306`]: The port of the server
* `nagios_plugin_percona_my_cnf_files.{n}.login_user`: [optional, default: `owner`]: The username used to authenticate with
* `nagios_plugin_percona_my_cnf_files.{n}.login_password`: [required]: The password used to authenticate with

* `nagios_plugin_percona_my_cnf_files.{n}.ssl`: [optional]: Whether or not to use SSL when connection

## Dependencies

None

## Recommended

* `nagios-server` ([see](https://github.com/Oefenweb/ansible-nagios-server))

#### Example(s)

##### Simple

```yaml
---
- hosts: all
  roles:
    - nagios-plugin-percona
```

##### With .my.cnf file(s)

```yaml
---
- hosts: all
  roles:
    - nagios-plugin-percona
  vars:
    nagios_plugin_percona_my_cnf_files:
      - dest: '~root/.my.cnf'
        owner: root
        group: root
        mode: '0600'
        login_host: localhost
        login_port: 3306
        login_user: root
        login_password: 'pw4Root'

      - owner: vagrant
        login_password: 'pw4Vagrant'
```

#### License

MIT

#### Author Information

Mark van Driel
Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-nagios-plugin-percona/issues)!
