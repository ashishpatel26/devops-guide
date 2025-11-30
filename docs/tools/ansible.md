# Ansible Cheat Sheet

Ansible is a configuration management and automation tool.

## Basic Commands

| Command | Description |
| :--- | :--- |
| `ansible all -m ping` | Ping all hosts in inventory |
| `ansible-playbook playbook.yml` | Run a playbook |
| `ansible-galaxy init <role>` | Initialize a new role |

## Inventory

Save as `hosts.ini`:

```ini
[webservers]
192.168.1.10
192.168.1.11

[dbservers]
192.168.1.20
```

## Playbook Example

Save as `playbook.yml`:

```yaml
---
- name: Install Nginx
  hosts: webservers
  become: yes
  tasks:
    - name: Ensure Nginx is installed
      apt:
        name: nginx
        state: present
    - name: Ensure Nginx is running
      service:
        name: nginx
        state: started
```