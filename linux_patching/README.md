# linux_patching

An Ansible role to perform safe Linux patching across multiple distributions.

## Supported Platforms
- RedHat / RHEL / CentOS / Rocky / Alma
- Ubuntu
- SUSE Linux Enterprise Server

## Features
- OS patching automation
- Rolling updates using serial execution
- Controlled reboot support
- Safe defaults (no reboot unless enabled)

## Role Variables

| Variable | Default | Description |
|--------|---------|-------------|
| patching_reboot | false | Enable reboot after patching |
| kernel_cleanup | false | Remove old kernels |
| reboot_timeout | 900 | Wait time for reboot (seconds) |

## Example Playbook

```yaml
- hosts: linux
  become: yes
  roles:
    - linux_patching
