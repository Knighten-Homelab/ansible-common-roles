# Ansible Common Roles Collection

A collection of reusable Ansible roles for homelab infrastructure management, focusing on system configuration and package manager proxy setup.

## Overview

This Ansible Galaxy collection (`homelab.common_roles`) provides common infrastructure roles that can be shared across multiple homelab projects. The collection includes roles for configuring package managers to use Nexus repository mirrors and basic system management tasks.

## Installation

### From Ansible Galaxy

```bash
ansible-galaxy collection install homelab.common_roles
```

### From Source

```bash
git clone https://github.com/Johnny-Knighten/ansible-homelab-common-roles
cd ansible-homelab-common-roles
ansible-galaxy collection build
ansible-galaxy collection install homelab-common_roles-*.tar.gz
```

## Roles

### Nexus Mirror Roles

Configure package managers to use a Nexus repository mirror:

- **[apt_nexus_mirror](roles/apt_nexus_mirror/README.md)** - Configure APT for Debian/Ubuntu systems
- **[pip_nexus_mirror](roles/pip_nexus_mirror/README.md)** - Configure pip Python package manager
- **[dockerhub_nexus_mirror](roles/dockerhub_nexus_mirror/README.md)** - Configure Docker registry mirror

All Nexus mirror roles default to `nexus.knighten.io` but can be configured to use any Nexus server via the `*_nexus_base_url` variable.

### System Management Roles

- **[disable_user](roles/disable_user/README.md)** - Lock user accounts and disable SSH access
- **[set_hostname](roles/set_hostname/README.md)** - Set system hostname

## Quick Start

### Example Playbook

```yaml
---
- name: Configure homelab servers
  hosts: all
  become: true

  roles:
    # Configure package managers to use Nexus
    - role: homelab.common_roles.apt_nexus_mirror
    - role: homelab.common_roles.pip_nexus_mirror
    - role: homelab.common_roles.dockerhub_nexus_mirror

    # Set hostname
    - role: homelab.common_roles.set_hostname
      vars:
        set_hostname_hostname: "{{ inventory_hostname }}"
```

### Custom Nexus Server

```yaml
---
- name: Configure with custom Nexus server
  hosts: all

  roles:
    - role: homelab.common_roles.apt_nexus_mirror
      vars:
        apt_nexus_mirror_nexus_base_url: "nexus.example.com"

    - role: homelab.common_roles.pip_nexus_mirror
      vars:
        pip_nexus_mirror_nexus_base_url: "nexus.example.com"
```

## Requirements

- Ansible >= 2.17.0
- Python >= 3.11 (for development)

## Development

See [CLAUDE.md](CLAUDE.md) for detailed development instructions including:
- Setting up the development environment with uv
- Running ansible-lint
- Conventional commit guidelines
- Release process

### Quick Development Setup

```bash
# Install uv
pip install uv

# Sync dependencies
uv sync

# Lint roles
uv run ansible-lint roles
```

## Documentation

Each role includes comprehensive documentation:
- Role-specific README with usage examples
- Variable descriptions and defaults
- Example playbooks

## License

Apache-2.0

## Author

Johnny Knighten

## Links

- [GitHub Repository](https://github.com/Johnny-Knighten/ansible-homelab-common-roles)
- [Issue Tracker](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/issues)
