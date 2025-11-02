# disable_user

Locks a user account and disables SSH access.

## Description

This role securely disables a user account by locking the password and removing SSH authorized keys. This is useful for decommissioning user accounts while preserving the user's home directory and files.

## Requirements

- Ansible >= 2.17

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `disable_user_name` | **Required** | Username of the account to disable |

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.disable_user
      vars:
        disable_user_name: "olduser"
```

### Disable Multiple Users

```yaml
- hosts: all
  tasks:
    - name: Disable multiple user accounts
      include_role:
        name: homelab.common_roles.disable_user
      vars:
        disable_user_name: "{{ item }}"
      loop:
        - user1
        - user2
        - user3
```

## What This Role Does

1. Locks the user account password
2. Removes the user's SSH authorized_keys file

## What This Role Does NOT Do

- Delete the user account
- Remove the user's home directory
- Kill active sessions
- Remove user from groups

## License

Apache-2.0

## Author

Johnny Knighten
