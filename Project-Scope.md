# 📌 Project Scope – Enterprise Network Infrastructure

## 🎯 Objective
The objective of this project is to design, implement, and validate a secure, scalable, and fully segmented multi-site enterprise network infrastructure that connects the Headquarters (HQ) with multiple branch offices through secure IPsec VPN tunnels, integrates a dedicated DMZ zone, delivers centralized authentication via Cisco ISE, and ensures continuous availability through firewall HA clustering.
The solution replicates a real-world enterprise environment with advanced routing, switching, security, and server services deployed end-to-end.
__________________________________________________________________________________________________________________________

## 🏢 Scope of Work
1. Enterprise Network Architecture & Segmentation
Design a hierarchical enterprise network including Core, Distribution, and Access layers.
Implement structured VLAN segmentation for HR, Sales, Finance, Media, and IT departments at both HQ and branches.
Apply uniform VLAN IDs across all branch offices for consistency.
Deploy a structured IP addressing plan using /27 subnets for departments and /30 point-to-point networks for WAN links.
Design routed connectivity between HQ and branch routers.
___________________________________________________________________
2. FortiGate NGFW Deployment & Security
Deploy FortiGate NGFW as the primary security and routing layer at HQ and branches.

Configure:
Inter-VLAN routing
NAT
Security policies
IPS, Antivirus, Web Filtering
Logging and monitoring
SNMP configuration
Enforce strict segmentation between:
User VLANs
IT Management
DMZ zone
Branch networks
Apply VIPs, service objects, Internet-service based policies, and granular access rules.
___________________________________________________________________
3. WAN Connectivity, SD-WAN & Branch Integration

Establish secure WAN connectivity between HQ and branch routers using IPsec VPN tunnels carried over routed WAN interfaces.
Configure SD-WAN combining:
WAN-ISP (port3)
WAN2 (port6)
for load balancing and link redundancy.
Ensure:
Branch access to HQ internal resources
Controlled DMZ access
Full segmentation (branch-to-branch isolation)
___________________________________________________________________

4. DMZ Zone Deployment

A dedicated DMZ subnet 10.20.20.0/27 hosts enterprise services, including:
-Web Server (IIS)
-SMTP
-FTP
-SMB File Services
-DHCP
-DNS
-NTP
-SNMP
-Syslog Server
-DMZ → internal traffic is tightly filtered using FortiGate firewall policies.
___________________________________________________________________

5. Centralized Authentication – Cisco ISE

Deploy Cisco ISE in the IT Management Network (192.168.10.0/24).
Implement AAA, TACACS+, RADIUS/802.1X, and endpoint identity enforcement.
Integrate ISE with:
Active Directory
FortiGate NGFW
Access switches
Management systems
Enforce identity-based access and device profiling.
___________________________________________________________________

6. Server Infrastructure & Enterprise Services

Windows Server 2016 deployed in the environment providing:
Active Directory Domain Services
DHCP Scopes for all HQ and Branch VLANs
DNS
Certificate Authority (CA)
NTP
SMTP
FTP
SMB / File Services
SNMP
Syslog
These services support:
Centralized identity
Automated IP addressing
Time synchronization
Logging and monitoring
Secure certificate distribution
___________________________________________________________________

7. High Availability (HA) & Redundancy

Deploy a FortiGate Active-Passive HA Cluster at HQ.
Configure:
Heartbeat links
Full config synchronization
Automatic failover
HQ switching redundancy provided using:
HSRP for gateway failover
EtherChannel for link aggregation
MST for spanning tree optimization
___________________________________________________________________

8. Dynamic Routing, Switching Security & Network Controls

Implement OSPF as the dynamic routing protocol between firewall, routers, and core switches.
Apply L2 security controls:
Port Security
DHCP Snooping
Dynamic ARP Inspection
BPDU Guard
Root Guard
Utilize ACLs to restrict inter-departmental traffic and protect sensitive segments such as:
Management
DMZ
Servers
___________________________________________________________________

9. System Validation & Testing

Perform complete functional testing including:
Inter-VLAN routing according to security policies
Branch-to-HQ reachability
DMZ service access
DHCP address distribution across departments
ISE Authentication and Authorization
Security policy enforcement (IPS/AV/Web Filtering)
Full HA failover simulation with zero downtime
___________________________________________________________________

10. Documentation & Final Deliverables

The final project deliverables include:
Full enterprise network topology diagrams (HQ & Branch)
Complete IP addressing and subnetting plan
VLAN tables and tagging structure
Routing configuration (Static + OSPF)
HA Cluster configuration
Firewall security policies
DMZ deployment documentation
Cisco ISE integration guide
Test results and validation logs
Final professional enterprise report (as in the uploaded DOCX)
__________________________________________________________________________________________________________________________


## ✅ Deliverables
- Complete network topology diagram.
- Device configurations (Switches, Routers, FortiGate).
- Documentation of VLANs, IP addressing, and subnetting plan.
- Security policy definitions and firewall configurations.
- Connectivity test results (ping, ACL, VPN).
