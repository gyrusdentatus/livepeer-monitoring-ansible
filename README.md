Role Name
=========

An Ansible role to deploy monitoring for Livepeer

Requirements
------------

Tested with Ansible 2.11.0

Role Variables
--------------

Ignore the defaults for now

Dependencies
------------

- Grafana running as a systemd service

Example Playbook
----------------

Draft of example playbook:

```yaml
---
- name: nvidia_exporter role
  hosts: all
  remote_user: root
  roles: 
    - nvidia_exporter
```
Tags: install, systemd

License
-------

BSD

Author Information
------------------

@hansbricks on Telegram and Keybase
