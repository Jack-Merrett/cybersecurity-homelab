# WireGuard VPN

> A self-hosted WireGuard VPN running in Docker, providing secure remote access to my Proxmox homelab from laptops, mobile devices, and a travel router.

---

## Overview

This project documents the deployment and configuration of a WireGuard VPN server hosted within my homelab. The VPN allows encrypted remote access to internal infrastructure without exposing management services directly to the internet.

The primary goal of this project was to gain hands-on experience with VPN technologies, secure remote administration, Docker networking, firewall configuration, and network troubleshooting.

---

## Objectives

- Deploy WireGuard using Docker
- Configure secure remote access
- Integrate Dynamic DNS
- Configure NAT and IP forwarding
- Support multiple VPN clients
- Enable secure administration while travelling
- Document the deployment process

---

## Lab Environment

| Component | Technology |
|-----------|------------|
| Hypervisor | Proxmox VE |
| Host OS | Ubuntu Server |
| Container Platform | Docker |
| VPN | WireGuard |
| Dynamic DNS | FreeMyIP |
| Firewall | iptables |
| Router | Ubiquiti |
| Remote Client | Windows Laptop |
| Travel Router | GL.iNet |

---

## Network Overview

```

Internet
│
▼
ISP Router
│
UDP 51820
│
▼
WireGuard Docker Container
│
VPN Tunnel
│
───────────────
│
├── Proxmox
├── Docker Services
├── Pi-hole
├── Wazuh
└── Internal Network

```

---

## Features

- Secure encrypted VPN
- Full-tunnel routing
- Dynamic DNS support
- Docker deployment
- Multiple client support
- Mobile access
- Travel router integration
- Persistent peer configuration

---

## Repository Structure

```

wireguard/
│
├── README.md
├── installation.md
├── setup.md
├── troubleshooting.md
└── japan-travel-router.md

```

---

## Documentation

| Document | Description |
|----------|-------------|
| Installation | Initial deployment process |
| Setup | Configuration and administration |
| Troubleshooting | Common issues and solutions |
| Japan Travel Router | Connecting a travel router while abroad |

---

## Skills Demonstrated

- Docker
- Linux Administration
- VPN Deployment
- WireGuard
- Routing
- NAT
- Firewall Configuration
- Port Forwarding
- Dynamic DNS
- Network Troubleshooting
- Secure Remote Access

---

## Lessons Learned

Building this project reinforced several networking concepts that are difficult to learn from theory alone. Configuring NAT, port forwarding, and IP forwarding helped me better understand packet flow through a VPN. Troubleshooting failed handshakes and routing issues also provided practical experience diagnosing network connectivity problems.

The project also demonstrated the importance of documentation, repeatable deployments, and securing infrastructure through encrypted remote access instead of exposing management interfaces directly to the public internet.

---

## Future Improvements

- Multi-factor authentication
- High availability
- IPv6 optimization
- Site-to-site VPN
- Prometheus monitoring
- Grafana dashboards
- Automated backups
- Configuration management with Ansible

---

## Screenshots

### Admin Interface

*(Add screenshots here after removing sensitive information.)*

---

## Disclaimer

This repository documents a personal homelab created for educational purposes. Any sensitive information including keys, IP addresses, domains, and credentials has been removed or anonymized.
