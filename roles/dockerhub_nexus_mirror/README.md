# dockerhub_nexus_mirror

Configures Docker to use a Nexus Docker registry mirror.

## Description

This role configures Docker daemon to use a Nexus repository as a registry mirror for Docker Hub. It sets up both the registry mirror and marks it as an insecure registry (suitable for internal network use). After configuration, Docker is automatically restarted to apply changes.

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `dockerhub_nexus_mirror_nexus_base_url` | `nexus.example.com` | Base URL for the Nexus server |
| `dockerhub_nexus_mirror_registry_port` | `8443` | Port for the Docker registry mirror |

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.dockerhub_nexus_mirror
```

### Custom Nexus Server

```yaml
- hosts: all
  roles:
    - role: homelab.common_roles.dockerhub_nexus_mirror
      vars:
        dockerhub_nexus_mirror_nexus_base_url: "nexus.example.com"
        dockerhub_nexus_mirror_registry_port: "5000"
```

## Handlers

- `Restart Docker` - Restarts the Docker service when configuration changes
