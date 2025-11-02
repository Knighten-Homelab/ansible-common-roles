# set_hostname

Sets the system hostname.

## Description

This role configures the system hostname using Ansible's built-in hostname module. The change persists across reboots.

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `set_hostname_hostname` | **Required** | The hostname to set for the system |

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.set_hostname
      vars:
        set_hostname_hostname: "webserver01"
```

### Set Different Hostnames per Host

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.set_hostname
      vars:
        set_hostname_hostname: "{{ inventory_hostname }}"
```

## Notes

- Requires privilege escalation (uses `become: true`)
- Changes take effect immediately
- Hostname persists across reboots
