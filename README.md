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
        │                                │
   OPNsense VM                   AdGuard Home
 (Router/Firewall)                     LXC
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
| OpenWrt | Wi-Fi Access Point | Cancelled |
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

- CPU: Intel i5 6th - 8th generation OR AMD Ryzen 5 2nd - 5th generation
- RAM: 16 GB 
- Storage: 256-500GB SSD
- Ethernet Ports: 2 built in OR install Network Interface Card (NIC)
- Wi-Fi Adapter: USB Wifi Adapter (Will need to research compatibility with OpenWRT)

---

# Build Log

## Step 1 — Purchase Mini PC

- [x] Research hardware
- [x] Purchase mini PC
- [ ] Install RAM (if needed)
- [ ] Install SSD (if needed)
- [ ] Install NIC (if needed)

Notes:
- Purchased a used HP PRODESK 400 G4 i5-8500T @ 2.1GHz, 16GB RAM with NO HDD/OS, will be supplying the PC with a used SSD from work
- For cost, most likely will purchase a USB-Ethernet Adaptor to act as second ethernet port for router
- Also for cost, will be abandonnning

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

## Deploy OpenWrt (Abandoned Project)

- [ ] Create VM
- [ ] Configure AP Mode
- [ ] Connect USB Wi-Fi adapter
- [ ] Test wireless clients

Notes:
## OpenWrt Hardware Evaluation

While planning the wireless networking portion of my homelab, I evaluated using a USB Wi-Fi adapter with OpenWrt compatibility versus purchasing a dedicated travel router.

### USB Wi-Fi Adapter Option
- Researched USB Wi-Fi adapters with chipsets supported by OpenWrt.
- Found that reliable adapters with good Linux/OpenWrt driver support typically cost around $35.
- While functional, USB adapters introduce additional considerations such as driver compatibility, antenna performance, and reduced reliability compared to dedicated networking hardware.

### GL.iNet Opal Alternative
After comparing costs and capabilities, I selected the GL.iNet Opal travel router as the more practical solution.

At approximately $40, the Opal provides:
- A dedicated OpenWrt-based networking platform.
- Built-in WireGuard/OpenVPN support.
- Travel router functionality including repeater, access point, and router modes.
- A more polished and reliable networking experience compared to using a USB Wi-Fi adapter.
- Small form factor, which fits original goal of minimizing space requirements.

The Opal can integrate with my existing homelab infrastructure by providing secure remote access through VPN connectivity and routing traffic to internal services such as DNS filtering through AdGuard Home/Pi-hole and other self-hosted services.

### Decision
The GL.iNet Opal was selected because it provided greater functionality, reliability, and ease of deployment for a similar cost compared to a USB Wi-Fi adapter. If I already had a compatible USB to Wifi adaptor on hand, this decision may have been different.  


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
