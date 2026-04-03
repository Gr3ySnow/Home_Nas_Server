# NAS Project

A home NAS setup running **OpenMediaVault (OMV)** as a virtual machine.

## Overview

This repository documents the configuration, setup process, and maintenance notes for my home NAS.

## Host & VM Setup

| Item         | Details                          |
|--------------|----------------------------------|
| Hypervisor   | Proxmox Ve                       |
| Host OS      | Debian 13.0                      |
| Guest OS     | <!-- e.g. OpenMediaVault 7.x --> |
| vCPUs        | <!-- e.g. 2 -->                  |
| RAM          | <!-- e.g. 4 GB -->               |
| Network      | <!-- e.g. Bridged adapter -->    |
| VM Disk      | <!-- e.g. 32 GB (OS only) -->    |

## Storage

| Drive | Size | Purpose | Pass-through? |
|-------|------|---------|---------------|
| <!-- e.g. /dev/sdb --> | <!-- 64 TB --> | <!-- Media --> | <!-- Yes --> |

## Services Running

- [ ] Samba (Windows file sharing)
- [ ] SSH
- [ ] FTP/SFTP
- [ ] Plex / Jellyfin
- [ ] Docker / Portainer
- [ ] Other: <!-- add here -->

## Network

- **NAS IP:** <!-- e.g. 192.168.1.x (static) -->
- **OMV Web UI port:**  <!-- 8080 : 80 -->
- **Hostname:** <!-- e.g. nas.local -->

## Initial Setup Notes

1. Downloaded OMV ISO from [openmediavault.org](https://www.openmediavault.org)
2. Created VM in <!-- hypervisor name -->
3. Passed through storage drives via <!-- e.g. USB controller / virtual disk -->
4. Installed OMV and ran initial configuration
5. <!-- Add your own steps -->

## Maintenance

- **Backups:** <!-- Describe your backup strategy -->
- **Updates:** <!-- How/when you update OMV -->
- **Monitoring:** <!-- e.g. OMV dashboard, Netdata, etc. -->

## Useful Commands

```bash
# SSH into the NAS
ssh admin@<NAS_IP>

# Check OMV service status
sudo systemctl status openmediavault-engined

# Apply pending OMV config changes from CLI
sudo omv-salt deploy run --follow
```

## Resources

- [OpenMediaVault Docs](https://docs.openmediavault.org)
- [OMV Community Forum](https://forum.openmediavault.org)
- [OMV-Extras Plugin](https://wiki.omv-extras.org)




