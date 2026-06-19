# Pi-hole Setup

## Objective

Deploy Pi-hole inside Docker to provide network-wide DNS filtering and advertisement blocking for all devices connected to the home network.

---

## Environment

Host:
- Ubuntu Server 24.04
- Docker
- Docker Compose

Hardware:
- Dell OptiPlex 7070

Network:
- LAN
- Static IP

---

## Prerequisites

- Docker installed
- Docker Compose installed
- Static IP assigned
- Port 53 available

---

## Installation

Clone repository

```bash
git clone https://github.com/pi-hole/docker-pi-hole.git
```

Start container

```bash
docker compose up -d
```

---

## Configuration

DNS Server:
192.168.1.10

Upstream DNS:
Cloudflare
1.1.1.1

Blocklists:

- StevenBlack
- OISD

Enabled:

- DHCP Disabled
- Conditional Forwarding Enabled

---

## Verification

Test DNS

```bash
nslookup google.com
```

Verify dashboard statistics.

Confirm advertisements are blocked on client devices.

---

## Security Considerations

Container runs on isolated Docker network.

Administrative dashboard protected with strong password.

Automatic updates performed manually after testing.

---

## Troubleshooting

Issue:

DNS not resolving.

Possible Causes

- Port 53 already in use
- Incorrect Docker networking
- Router still pointing to ISP DNS

Resolution

Check

```bash
docker logs pihole
```

Verify router DNS settings.

---

## Lessons Learned

Docker networking conflicts are usually responsible for DNS failures.

Keeping Pi-hole isolated from other containers simplifies troubleshooting.

---

## Future Improvements

- Add secondary Pi-hole
- High Availability
- DNS over HTTPS
