# Proxmox-Homelab

Transforming a used business-class mini PC into a Proxmox-powered homelab. The goal is to virtualize core networking services (OpenWrt/OPNsense, AdGuard Home), provide Wi-Fi access, and gradually expand into self-hosting, network monitoring, security, and automation.

---

# Disclaimer

This project is intended for **learning and homelab purposes**.

To minimize hardware costs and space requirements, multiple critical services are consolidated onto a single physical machine using Proxmox. While separating these services across dedicated devices can improve redundancy and fault isolation, this project prioritizes hands-on learning, experimentation, and efficient resource usage.

If the Proxmox host goes offline, all virtualized services will also become unavailable.

---

# Objectives

This project aims to gain hands-on experience with:

- Proxmox VE
- Virtualization
- Linux administration
- Networking
- Routing & Firewalls
- DNS
- Self-hosting
- Infrastructure documentation
- Network security

---

# Planned Architecture

```
                    Internet
                        │
                   ISP Modem
                        │
                 Family Router
           (Existing home network)
                        │
                 Mini PC (WAN)
                        │
                   Proxmox VE
                        │
        ┌───────────────┼────────────────┐
        │               │                │
   OPNsense VM     OpenWrt VM      AdGuard Home
 (Router/Firewall) (Wi-Fi AP)          LXC
        │
     Private LAN
        │
  ┌─────┴──────────────┐
  │                    │
 Laptop            Other Devices
```

---

# Planned Services

| Service | Purpose | Status |
|----------|---------|--------|
| Proxmox VE | Hypervisor | Planned |
| OPNsense | Router / Firewall | Planned |
| OpenWrt | Wi-Fi Access Point | Planned |
| AdGuard Home | DNS Filtering | Planned |
| Ubuntu/Debian VM | General-purpose Linux server for Docker, testing, and development | Planned |
| Docker | Container platform for self-hosted applications | Future |
| Uptime Kuma | Service and network monitoring | Future |
| Prometheus | Metrics collection and monitoring | Future |
| Grafana | Metrics dashboards and visualization | Future |
| Firefly III | Finance Tracking | Future |
| Jellyfin | Media Server | Future |



---

# Hardware

## Mini PC

*(Insert photo here)*

### Planned Specifications

- CPU:
- RAM:
- Storage:
- Ethernet Ports:
- Wi-Fi Adapter:

---

# Build Log

## Step 1 — Purchase Mini PC

- [ ] Research hardware
- [ ] Purchase mini PC
- [ ] Install RAM (if needed)
- [ ] Install SSD (if needed)
- [ ] Install NIC (if needed)

Notes:

---

## Step 2 — Install Proxmox VE

- [ ] Create bootable USB
- [ ] Install Proxmox
- [ ] Configure storage
- [ ] Configure management interface
- [ ] Enable updates

Notes:

---

## Step 3 — Configure Networking

- [ ] Create Linux bridge
- [ ] Configure WAN interface
- [ ] Configure LAN interface
- [ ] Verify internet connectivity

Notes:

---

## Step 4 — Deploy OPNsense

- [ ] Create VM
- [ ] Assign WAN/LAN interfaces
- [ ] Configure DHCP
- [ ] Configure firewall rules
- [ ] Create WireGuard VPN

Notes:

---

## Step 5 — Deploy OpenWrt

- [ ] Create VM
- [ ] Configure AP Mode
- [ ] Connect USB Wi-Fi adapter
- [ ] Test wireless clients

Notes:

---

## Step 6 — Deploy AdGuard Home

- [ ] Create LXC
- [ ] Configure DNS
- [ ] Point clients to AdGuard
- [ ] Test DNS filtering

Notes:

---

# Future Plans
- Network Monitoring
- Automated Backups
- Ansible
- Reverse Proxy
- Docker
- Uptime Kuma
- Prometheus
- Grafana
- NAS
- VLANs
- IDS/IPS


---

# Skills Learned

- Proxmox VE
- Linux
- Virtual Machines
- LXC Containers
- Routing
- NAT
- DHCP
- DNS
- Firewalls
- VLANs
- Network Security
- Self-hosting
- Infrastructure Documentation
