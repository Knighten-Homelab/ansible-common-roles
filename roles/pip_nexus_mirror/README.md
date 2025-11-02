# pip_nexus_mirror

Configures pip to use a Nexus PyPI repository proxy.

## Description

This role configures the system-wide pip configuration file (`/etc/pip.conf`) to use a Nexus repository as the PyPI index. This allows for faster package installations and centralized package management in air-gapped or restricted network environments.

## Requirements

- Ansible >= 2.17

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `pip_nexus_mirror_nexus_base_url` | `nexus.knighten.io` | Base URL for the Nexus server |
| `pip_nexus_mirror_index` | `http://{{ nexus_base_url }}/repository/pypi-proxy/pypi` | PyPI index URL |
| `pip_nexus_mirror_index_url` | `http://{{ nexus_base_url }}/repository/pypi-proxy/simple` | PyPI simple index URL |
| `pip_nexus_mirror_host` | `{{ nexus_base_url }}` | Trusted host for pip |

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.pip_nexus_mirror
```

### Custom Nexus Server

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.pip_nexus_mirror
      vars:
        pip_nexus_mirror_nexus_base_url: "nexus.example.com"
```

## License

Apache-2.0

## Author

Johnny Knighten
