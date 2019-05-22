gearman_exporter
================

Ansible role for install Prometheus exporter that exports Gearman status.

Requirements
------------

Ansible.  
amd64 arch.

Role Variables
--------------

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `gearman_exporter_version` | 0.5.0 | gearmanexporter package version. |
| `gearman_exporter_web_listen_address` | "0.0.0.0:9418" | Address on which gearman_exporter will listen |
| `gearman_exporter_gearmand_adress` | "127.0.0.1:4730" | Address on which gearmand is accessible |

Dependencies
------------

None.

Example Playbook
----------------

Use it in a playbook as follows:

```yaml
- hosts: all
  become: yes
  roles:
    - gearman_exporter
```

Configuration notes
-------------------

About usage of gearman_exporter check:  
https://github.com/bakins/gearman-exporter/blob/master/README.md

License
-------

BSD

Credits
-------

This role is inspired by https://github.com/cloudalchemy/ansible-mysqld-exporter  
gearman-exporter is created by bakins (https://github.com/bakins/gearman-exporter) and this is only wrap-up in Ansible role.
