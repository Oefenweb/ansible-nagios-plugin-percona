## nagios-plugin-percona

[![Build Status](https://travis-ci.org/Oefenweb/ansible-nagios-plugin-percona.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-nagios-plugin-percona)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-nagios--plugin--percona-blue.svg)](https://galaxy.ansible.com/Oefenweb/nagios-plugin-percona)

Set up [Percona Monitoring Plugins](https://www.percona.com/software/mysql-tools/percona-monitoring-plugins) for Nagios in Debian-like systems.

#### Requirements

None

#### Variables

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
