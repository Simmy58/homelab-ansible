# Homelab Ansible

Ansible project for managing and checking the homelab.

## Managed infrastructure

### Proxmox
| Host |
|---|
| prometheus |

### LXC containers
| Host |
|---|
| pihole |
| jellyfin |
| vaultwarden |
| immich |
| seerr |
| radarr |
| sonarr |
| prowlarr |
| qbittorrent |
| nginxproxymanager |
| cloudflared |
| tailscale |

## Project structure

- `ansible.cfg` - Ansible configuration
- `inventory/hosts.ini` - Managed hosts and groups
- `playbooks/update-lxcs.yml` - Updates Debian LXC containers
- `playbooks/health-check.yml` - Checks server health and disk usage

## Requirements

- Ansible installed on the management machine
- SSH access to managed hosts
- SSH private key at `~/.ssh/id_ed25519`
- Root SSH access on managed hosts

## Common commands

Run from `~/ansible`.

### Check connectivity

```bash
ansible all -m ping
