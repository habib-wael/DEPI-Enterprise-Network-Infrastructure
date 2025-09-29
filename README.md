# 📌 Project Scope – Enterprise Network Infrastructure

## 🎯 Objective
The main objective of this project is to design and implement a **secure, scalable, and highly available enterprise network** that connects multiple departments and branches under a unified infrastructure.

## 🏢 Scope of Work
- Design a hierarchical enterprise network with Core, Distribution, and Access layers.
- Implement **VLANs and subnetting** for departmental segmentation and efficient IP allocation.
- Deploy a **FortiGate Firewall** to enforce enterprise-wide security policies.
- Configure a **DMZ** for hosting critical servers and services.
- Establish **VPN tunnels** using **IPSec** for secure remote and branch connectivity.
- Integrate **Cloud services** to enhance scalability and flexibility.
- Configure **OSPF (Area 0 Backbone)** to connect HQ and Branch networks.
- Implement **HSRP** for Layer 3 redundancy and **MSTP** for loop prevention.

## ✅ Deliverables
- Complete network topology diagram.
- Device configurations (Switches, Routers, FortiGate).
- Documentation of VLANs, IP addressing, and subnetting plan.
- Security policy definitions and firewall configurations.
- VPN configuration details with IPSec parameters.
- High availability plan (HSRP + EtherChannel).
- Connectivity test results (ping, ACL, VPN).
- # 🖧 Network Design Details

## 🔹 VLAN & Subnetting Plan
| Department            | VLAN ID | HQ Subnet        | Branch Subnet    | Host Range  |
|-----------------------|---------|------------------|------------------|-------------|
| IT & Management       | 10      | 192.168.10.0/24 | 192.168.110.0/24 | 1 – 254     |
| Human Resources (HR)  | 20      | 192.168.20.0/27 | 192.168.120.0/27 | 1 – 30      |
| Sales                 | 30      | 192.168.30.32/27| 192.168.130.32/27| 33 – 62     |
| Finance & Accounting  | 40      | 192.168.40.64/27| 192.168.140.64/27| 65 – 94     |
| Media                 | 50      | 192.168.50.96/27| 192.168.150.96/27| 97 – 126    |

## 🔄 Redundancy
- **EtherChannel (LACP)** configured between core and distribution switches.
- **HSRP** configured on multilayer switches for default gateway redundancy.
- **MSTP** implemented to prevent loops with HQ switch as Root Bridge.

## 🔒 Security Features
- **FortiGate Firewall** enforcing NAT, VPN, and ACL policies.
- **Static NAT** for Internet access through FortiGate.
- **DMZ** separating enterprise servers (Web, Syslog, DHCP).
- ACLs restricting access between VLANs.

## 🌍 Connectivity
- **OSPF Area 0 backbone** connecting HQ and Branch.
- Site-to-Site **IPSec VPN tunnels** between HQ and Branch.
- Default routes propagated for Internet access.
- Cloud connectivity enabled for scalability.

## ⚙ Services
- **Windows Server 2016** providing DHCP, DNS, and Web hosting.
- **Syslog Server** for centralized monitoring.
- **NTP Server** for time synchronization across devices.
- # 🔒 Security Policies

## LAN Security
- Port Security with violation actions.
- **BPDU Guard** and **Root Guard** enabled on access ports.
- **Dynamic ARP Inspection (DAI)** and **DHCP Snooping** configured.
- **Disable DTP** on access ports to prevent VLAN hopping attacks.

## WAN Security
- **IPSec VPN tunnels** for secure branch-to-branch communication.
- DES encryption and pre-shared keys for authentication.
- Tunnel mode for encapsulation.
- FortiGate firewall policies applied for WAN traffic filtering.

## Management Security
- **SSHv2** for secure device access.
- Centralized authentication using **ISE, RADIUS, and TACACS+**.
- Access control lists (ACLs) limiting management access to VTY lines.
- # ⚙ Network Services

## DHCP
- Centralized DHCP Server configured for both HQ and Branch VLANs.
- DHCP relay agents enabled on routers for remote VLANs.

## Routing (OSPF)
- **OSPF Area 0 (Backbone)** configured for HQ and Branch.
- Fast hello/dead timers enabled for rapid convergence.

## NAT
- **Static NAT** configured on FortiGate for Internet access.
- PAT for internal user Internet connectivity.

## VPN
- **Site-to-Site IPSec VPN tunnels** between HQ and Branch.
- DES encryption with pre-shared keys.
- Tunnel mode providing secure encapsulation.

## Syslog
- Centralized Syslog server collecting logs from all devices.
- Alerts configured for security events and violations.

## NTP
- Dedicated NTP server for synchronized time across devices.
- Ensures accurate timestamps for logs and monitoring.

## High Availability
- Dual links between switches with **EtherChannel** for load balancing.
- **HSRP** configured for default gateway redundancy.
