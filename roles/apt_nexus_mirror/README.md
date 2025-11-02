# apt_nexus_mirror

Configures APT package manager to use a Nexus repository mirror for Debian and Ubuntu systems.

## Description

This role backs up existing APT sources, clears all current repository configurations, and configures the system to use Nexus repository proxies. It supports both Ubuntu (Jammy) and Debian (Bookworm) distributions with distribution-specific repository sources.

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `apt_nexus_mirror_nexus_base_url` | `nexus.example.com` | Base URL for the Nexus server |
| `apt_nexus_mirror_ubuntu_nexus_sources` | See defaults | List of Ubuntu repository source lines |
| `apt_nexus_mirror_debian_nexus_sources` | See defaults | List of Debian repository source lines |
| `apt_nexus_mirror_nexus_sources` | Auto-detected | Automatically selected based on distribution |

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.apt_nexus_mirror
```

### Custom Nexus Server

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.apt_nexus_mirror
      vars:
        apt_nexus_mirror_nexus_base_url: "nexus.example.com"
```

## Tags

- `backup` - Backup operations
- `cleanup` - Repository cleanup tasks
- `configure` - Repository configuration
- `update` - APT cache update
