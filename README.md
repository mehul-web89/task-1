
# Create User

A role for creating a Linux User.


## Requirements

This role depends on the variable Linux_user_pass which is mandatory to provide to complete the ansible role.

Below field should be provided to run the playbook.

Linux_user_pass: Legacy method of storing user password. Value should always be 'x' or '*'.


## Role Variables

user: Linux user will be created if it is not exists.

## Dependencies

It must provide 
## Example Playbooks

```bash

  playbook.yml:

---
- name: Creating a playbook with roles
  hosts: servers
  become: yes
  vars_prompt:
    - name: "Linux_user_pass"
      prompt: "Enter password"
      unsafe: yes
      private: yes
      confirm: yes
  roles:
    - role: create-user
```
