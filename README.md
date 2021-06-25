## nagios-plugin-percona

[![CI](https://github.com/Oefenweb/ansible-nagios-plugin-percona/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-nagios-plugin-percona/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-nagios--plugin--percona-blue.svg)](https://galaxy.ansible.com/Oefenweb/nagios_plugin_percona)

Set up [Percona Monitoring Plugins](https://www.percona.com/software/mysql-tools/percona-monitoring-plugins) for Nagios in Debian-like systems.

#### Requirements

* `software-properties-common` (will be installed)
* `dirmngr` (will be installed)
* `xz-utils` (will be installed when `nagios_plugin_percona_package_path_src` is defined)

#### Variables

* `nagios_plugin_percona_package_path_src`: [optional]: Path to deb package to install (e.g. `percona-nagios-plugins_1.1.9-635751136_all.deb`)
* `nagios_plugin_percona_install`: [default: `[]`]: Additional packages to install

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

#### License

MIT

#### Author Information

* Mark van Driel
* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-nagios-plugin-percona/issues)!
