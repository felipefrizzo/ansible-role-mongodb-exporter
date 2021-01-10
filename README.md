# Ansible MongoDB Exporter

## Description

Deploy prometheus [mongodb exporter](https://github.com/percona/mongodb_exporter) by Percona using ansible.  
This ansible role are based on [mongodb-exporter](https://github.com/kostiantyn-nemchenko/ansible-role-mongodb-exporter) and [node-exporter](https://github.com/cloudalchemy/ansible-node-exporter)

## Requirements

- Ansible >= 2.9

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) and are listed in the table below.
| Name | Default Value | Description |
| ---- | ------------- | ----------- |
| `mongodb_exporter_version` | 0.21.0 | MongoDB exporter package version |

## Playbook

Use it in a playbook as follows:

```yml
- hosts: all
  roles:
      - felipefrizzo.mongodb_exporter
```

## License

This project is licensed under MIT License. See LICENSE for more details.
