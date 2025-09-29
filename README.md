# 📌 Project Scope – Enterprise Network Infrastructure

## 🎯 Objective
The main objective of this project is to design and implement a **secure, scalable, and highly available enterprise network** that connects multiple departments and branches under a unified infrastructure.

## 🏢 Scope of Work
- Design a hierarchical enterprise network with Core, Distribution, and Access layers.
- Implement **VLANs and subnetting** for departmental segmentation and efficient IP allocation.
- Deploy a **FortiGate Firewall** to enforce enterprise-wide security policies.
- Configure a **DMZ** for hosting critical servers and services.
- Establish **VPN tunnels** for secure remote and branch connectivity.
- Integrate **Cloud services** to enhance scalability and flexibility.

## ✅ Deliverables
- Complete network topology diagram.
- Device configurations (Switches, Routers, FortiGate).
- Documentation of VLANs, IP addressing, and subnetting plan.
- Security policy definitions and firewall configurations.
- Connectivity test results (ping, ACL, VPN).
- # 🖧 Network Design Details

## 🔹 VLAN & Subnetting Plan
| Department         | VLAN ID | Subnet            | Gateway        |
|--------------------|---------|------------------|----------------|
| IT                 | 10      | 192.168.10.0/24  | 192.168.10.1   |
| Business           | 20      | 192.168.20.0/24  | 192.168.20.1   |
| Arts & Design      | 30      | 192.168.30.0/24  | 192.168.30.1   |
| Health & Sciences  | 40      | 192.168.40.0/24  | 192.168.40.1   |
| Servers (DMZ)      | 50      | 192.168.50.0/24  | 192.168.50.1   |

## 🔄 Redundancy
- **EtherChannel (LACP)** configured between core and distribution switches.
- Redundant uplinks between critical network devices.

## 🔒 Security Features
- **FortiGate Firewall** enforcing NAT, VPN, and ACL policies.
- **DMZ** separating enterprise servers (Web, Syslog, DHCP).
- ACLs restricting access between VLANs.

## 🌍 Connectivity
- Default routes advertised to ISP for Internet access.
- VPN tunnels configured for secure branch communication.
- Cloud connectivity enabled for scalability.

## ⚙ Services
- **Windows Server 2016** providing DHCP, DNS, and Web hosting.
- **Syslog Server** for centralized monitoring.
- **NTP Server** for time synchronization across devices.
- # 🔒 Security Policies

## FortiGate Firewall
- NAT & PAT rules for Internet access.
- VPN tunnels for branch-to-branch connectivity.
- ACLs controlling HTTP, HTTPS, FTP, and Syslog traffic.

## Switch Security
- Port Security with violation actions.
- Disabled CDP on sensitive ports.
- DHCP Snooping and Dynamic ARP Inspection (DAI).
- BPDU Guard enabled to protect Spanning Tree.

## User Access
- SSH enabled for secure device management.
- Role-based access for administrators.
- 802.1X Port-Based Authentication for endpoint security.
- # ⚙ Network Services

## DHCP
- Centralized DHCP Server with relay agents configured on routers.
- Dynamic allocation of IP addresses per VLAN.

## Syslog
- Centralized Syslog server to collect logs from all devices.
- Alerts configured for security and violation events.

## NTP
- Dedicated NTP server for time synchronization.
- Ensures accurate timestamps for logs and monitoring.

## Web Services
- Enterprise Web Server hosted in the DMZ.
- Accessible securely via firewall rules.

## Cloud Services
- Cloud integration for scalable applications.
- Supports hybrid environment for future expansion.
