# Ansible MongoDB Exporter

[![Molecule](https://github.com/felipefrizzo/ansible-role-mongodb-exporter/workflows/Molecule/badge.svg?event=push)](https://github.com/felipefrizzo/ansible-role-mongodb-exporter/actions?query=workflow%3AMolecule)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)

## Description

Deploy prometheus [mongodb exporter](https://github.com/percona/mongodb_exporter) by Percona using ansible.  
This ansible role are based on [mongodb-exporter](https://github.com/kostiantyn-nemchenko/ansible-role-mongodb-exporter) and [node-exporter](https://github.com/cloudalchemy/ansible-node-exporter)

## Requirements

- Ansible >= 2.9

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) and are listed in the table below.
| Name | Default Value | Description |
| ---- | ------------- | ----------- |
| `mongodb_exporter_version` | 0.20.1 | MongoDB exporter package version |
| `mongodb_exporter_binary_local_dir` | "" | Allows to use local packages instead of ones distributed on github. As parameter it takes a directory where mongodb_exporter binary is stored on host on which ansible is ran. This overrides mongodb_exporter_version parameter |
| `mongodb_exporter_web_listen_address` | "0.0.0.0:9216" | Address on which mongodb exporter will listen |
| `mongodb_exporter_web_telemetry_path` | "/metrics" | Path under which to expose metrics |
| `mongodb_exporter_database_uri` | "mongodb://127.0.0.1:27017" | MongoDB URI |
| `mongodb_exporter_collect_database` | false | Enable collection of Database metrics |
| `mongodb_exporter_collect_collection` | false | Enable collection of Collection metrics |
| `mongodb_exporter_collect_topmetrics` | false | Enable collection of table top metrics |
| `mongodb_exporter_collect_indexusage` | false | Enable collection of per index usage stats |

## Playbook

Use it in a playbook as follows:

```yml
- hosts: all
  roles:
      - felipefrizzo.mongodb_exporter
```

## License

This project is licensed under MIT License. See LICENSE for more details.
