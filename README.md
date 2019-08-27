# Ansible-goss
Ansible role for provisioning and verifying servers using goss.
## What is does
1. Installs Goss on host
1. Copies goss.yml over to host
1. Verifies host using Goss
1. Retrieves Goss results.json
## Playbook Example
```yaml
---
- name: "Install Vault"
  hosts: vault
  vars:
    vault_backend: file
    caller_directory: "{{ playbook_dir  }}"
    caller_name: ""
  any_errors_fatal: true
  become: true
  become_user: root
  roles:
    - brianshumate.vault
    - matttrach.goss
```
## Goss
https://github.com/aelsabbahy/goss
Static server testing, extremely easy to setup.
Gossadd and gossautoadd are the magic sauce that makes it just wonderful to use.
