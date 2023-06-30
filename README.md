
# Create User

A role for creating a Linux User on git.


## Requirements

This role depends on the variable Linux_user_pass which is mandatory to provide to complete the ansible role.

Below field should be provided to run the playbook.

Linux_user_pass: Legacy method of storing user password. Value should always be 'x' or '*'.

### Install

You need to include requirements.yml file and install it via ansible-galaxy install -r requirements.yml using the format:

Install it via ansible-galaxy (recommended):

```bash
ansible-galaxy install -r requirements.yml
```
###### *__NOTE__: Installing collections with ansible-galaxy is only supported in ansible 2.9+*


## Role Variables

user: Linux user will be created if it is not exists.

## Dependencies

Must provide below variable
- name: Linux_user_pass 

## Example Playbooks

```bash

playbook.yml:

---

- name: Creating a playbook with roles
  hosts: all
  vars_prompt:
    - name: "Linux_user_pass"
      prompt: "Enter password"
      private: yes
      confirm: yes
  roles:
    - role: task-1
```
