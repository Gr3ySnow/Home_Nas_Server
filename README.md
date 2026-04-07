# NAS Project

A home NAS setup running **OpenMediaVault (OMV)** as a virtual machine.

## Overview

This repository documents the configuration, setup process, and maintenance notes for my home NAS.

## Host & VM Setup

| Item         | Details                          |
|--------------|----------------------------------|
| Hypervisor   | Proxmox Ve                       |
| Host OS      | Debian 13.0                      |
| Guest OS     | OpenMediaVault 7.x               |
| vCPUs        | 3                                |
| RAM          | 5 GB                             |
| Network      | Bridged adapter                  |
| VM Disk      | 32 GB (OS only)                  |

## Storage

| Drive | Size | Purpose | Pass-through? |
|-------|------|---------|---------------|
|  /dev/sdb  | 64 GB  |  Media  |  Yes  |

## Services Running

- [x] SMB file share
- [x] SSH
- [x] Jellyfin
- [x] Docker / Portainer


## Network

- **NAS IP:**  192.168.1.73
- **OMV Web UI port:**  8080 : 80 
- **Hostname:** omv1.internal

## Initial Setup Notes

1. Downloaded OMV ISO from [openmediavault.org](https://www.openmediavault.org)
2. Created VM in Proxmox VE
3. Passed through storage drives via USB controller / virtual disk 
4. Installed OMV and ran initial configuration
5. Activated SMB file share and storage files
6. Created Jellyfin docker container and connected to network

## Maintenance

- **Backups:** Creation of backup folders 
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




