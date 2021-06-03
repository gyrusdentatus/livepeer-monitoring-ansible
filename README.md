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

```
$ ansible-playbook -i hosts playbooks/nvidia_exporter.yaml --list-tasks 

playbook: playbooks/nvidia_exporter.yaml

  play #1 (all): nvidia_exporter role   TAGS: []
    tasks:
      nvidia_exporter : Ensure Grafana is running       TAGS: [install]
      nvidia_exporter : Download nvidia_exporter.go     TAGS: [install]
      nvidia_exporter : Create the nvidia_exporter groups       TAGS: [install]
      nvidia_exporter : Create the nvidia_exporter user TAGS: [install]
      nvidia_exporter : go build nvidia_exporter        TAGS: [install]
      nvidia_exporter : copy the nvidia_exporter binary to its destination      TAGS: [install]
      nvidia_exporter : install service script  TAGS: [install, systemd]
      nvidia_exporter : reload nvidia_exporter.service  TAGS: [install, systemd]
      nvidia_exporter : enable the service      TAGS: [install, systemd]
      nvidia_exporter : start service   TAGS: [install, systemd]
```



License
-------

BSD

Author Information
------------------

@hansbricks on Telegram and Keybase
