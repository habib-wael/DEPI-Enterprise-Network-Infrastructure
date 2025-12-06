# Graduation Project – Network Topology & Design

This repository contains the full network design and documentation for our graduation project.

## 1. Overview

- **Type:** Enterprise campus + branches
- **Vendor mix:** Cisco switches/routers + Fortinet FortiGate firewall + Windows Server 2016
- **Main services:**
  - Active Directory
  - DNS
  - DHCP
  - Web Server (HTTP/HTTPS)
  - FTP
  - NTP
  - SNMP
  - Syslog
  - Certificate Authority (CA)
  - FSSO Integration with FortiGate

## 2. Topology

The main topology is available in:

- `diagrams/Topology.png`

This diagram shows:

- HQ Core switches and distribution switches
- FortiGate firewall between Internal LAN and Internet
- DMZ network for servers
- Branch routers connected over IPsec VPN
- Separate VLANs for:
  - HR
  - Sales
  - Finance
  - Media
  - IT Management
  - Branch departments

## 3. Documentation

- [`docs/network-topology.md`](docs/network-topology.md)  
  High-level explanation of the physical and logical topology.

- [`docs/vlans-and-subnets.md`](docs/vlans-and-subnets.md)  
  VLAN IDs, subnetting plan, and addressing scheme (/27, /30, etc.).

- [`docs/routing-and-vpn.md`](docs/routing-and-vpn.md)  
  Static routes / dynamic routing (if used) and IPsec VPN design between HQ and branches.

## 4. Tools Used

- Microsoft Visio / draw.io for network diagram
- Cisco IOS for Layer 2 / Layer 3 switches and routers
- Fortinet FortiOS for firewall and VPN
- Windows Server 2016 for all server roles

## 5. Team

- Network Design & Security: <Your Name>
- Server Infrastructure: <Your Name / Team>
- Documentation: <Your Name>

> This repository is documentation-focused. Configuration files for the firewall and servers are stored in separate repositories.
