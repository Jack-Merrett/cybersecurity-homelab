# Project Name

## Objective

Wanted to create a secure VPN connection back to my home network while traveling. The original plan was to be able to appear like I am on my home network while being in a different state or abroad. 

This allows me too: 
- Access my homelab resourses remotely.
- Route Traffic throug my home network. 
- Use trusted DNS while visiting different states and abroad.
- Maintain access to self-hosted services.

## Architecture

Travel Router
      ↓
WireGuard Tunnel
      ↓
Home Network
      ↓
Proxmox / Docker / Wazuh

## Environment

Hardware:
- Ubiquity UniFi Travel Router 
- 

## Challenges Encountered

### Tunnel Would Not Establish

Problem:

Clients could not connect.

Root Cause:

UDP 51820 was blocked by the firewall.

Resolution:

Created inbound firewall rule.

## Lessons Learned

WireGuard troubleshooting usually involves:

- Firewall rules
- NAT
- Incorrect peer configuration
- Routing issues

Checking these first resolves most problems.