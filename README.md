#  Enterprise Network Security Infrastructure  
### **Graduation Project – DEPI | Fortinet Cybersecurity Track**

This repository contains the full design, implementation, and validation of a **secure, scalable, and fully segmented multi-site enterprise network infrastructure**.  
The project integrates **HQ**, **Branch Sites**, a **DMZ**, **IT Management Zone**, **Cisco ISE**, **Windows Server Services**, and **FortiGate NGFW**, all deployed and tested inside a virtualized GNS3 environment.

---

##  **1. Project Overview**

The goal of the project is to build a real-world enterprise network architecture that includes:

- End-to-end security  
- Segmentation & traffic isolation  
- High availability  
- Centralized identity & authentication  
- Secure WAN connectivity  
- Full monitoring, logging, and server services  

The network replicates an enterprise-grade environment using **advanced routing, switching, and security technologies**.

---

## 🎯 **2. Key Features**

### 🔐 **Security**
- FortiGate NGFW policies (IPS, AV, Web Filtering, SSL inspection)
- Next-generation traffic inspection
- DMZ segmentation & strict access rules
- SNMP, Syslog, and monitoring services
- Identity-based access with Cisco ISE
- IPsec VPN for branch connectivity

###  **Network Segmentation**
- Dedicated VLANs for HR, Sales, Finance, Media, and IT  
- Unified VLAN structure across all branches  
- Per-department subnetting using /27 networks  
- IT Management zone (192.168.10.0/24)

### 🌐 **WAN & Connectivity**
- SD-WAN configuration on FortiGate (dual WAN)  
- Branch to HQ secure tunnels via IPsec  
- Routed /30 links for WAN stability  
- Branch isolation enforcement

###  **Server Infrastructure**
Windows Server 2016 hosting:
- Active Directory (AD DS)  
- DHCP scopes for HQ + branches  
- DNS services  
- Certificate Authority (CA)  
- IIS Web Server  
- FTP  
- SMTP  
- NTP  
- SNMP  
- Syslog  

###  **High Availability**
- Active–Passive FortiGate HA cluster  
- HSRP redundancy for default gateway  
- EtherChannel for link aggregation  
- MST for spanning-tree optimization  

---

##  **3. Network Topology**

Main Topology Diagram:

> ![Topology](https://github.com/user-attachments/assets/6d3ca481-8cb7-44a7-a3a6-0a1d2c2cfd6b)



The topology includes:
- HQ Core & Distribution switches  
- FortiGate HA cluster  
- DMZ network  
- IT Management network  
- Cisco ISE  
- Branch networks (HR, Sales, Finance, Media, IT)  
- IPsec VPN tunnels  

---

##  **4. Technologies Used**

### **Networking**
- VLANs, Trunking, EtherChannel  
- OSPF Dynamic Routing  
- HSRP Gateway Redundancy  
- MST Spanning Tree  
- ACLs & Layer 2 Security  
- DHCP Snooping, DAI, Port Security  

### **Security**
- FortiGate NGFW  
- IPS / Antivirus / Web Filtering  
- SD-WAN  
- HA Clustering  
- SNMP Monitoring  
- Syslog Integration  

### **Identity**
- Cisco ISE  
- RADIUS (802.1X)  
- TACACS+  
- FSSO Integration  

### **Servers**
- Windows Server 2016  
- AD, DNS, DHCP  
- CA Services  
- IIS, FTP, SMTP  
- Syslog, NTP, SNMP  

---

##  **5. Project Scope Summary**

This project covers:

- Complete enterprise design (HQ + Branch + DMZ + Management)
- VLAN segmentation and subnetting
- Firewall policies, NAT, VIPs, service objects
- SD-WAN load balancing
- IPsec VPN tunnels for branches
- Cisco ISE deployment and AAA integration
- Windows Server services (AD, DNS, DHCP, FTP…)
- Layer 2 security controls
- High availability configurations (HA Cluster, HSRP)
- Full testing and validation

For the detailed scope:  
 See **Project-Scope.md**

---

##  6. Repository Structure

```
📁 Enterprise-Network-Infrastructure/
│
├── Project-Scope.md              # Full written scope & documentation
├── README.md                     # Repository introduction
│
├── diagrams/
│   └── Topology.png              # Network topology diagram
│
├── configs/
│   ├── FortiGate/                # HQ & Branch firewall configs
│   ├── Cisco_Switches/           # VLANs, EtherChannel, HSRP...
│   └── Routers/                  # WAN + OSPF configs
│
├── servers/
│   ├── AD_DS.md                  # Active Directory setup
│   ├── DHCP.md                   # DHCP scopes
│   ├── DNS.md                    # DNS structure
│   ├── CA.md                     # Certificate Authority
│   ├── IIS.md                    # Web server (IIS)
│   ├── FTP.md                    # FTP server
│   ├── Syslog.md                 # Syslog configuration
│   └── NTP.md                    # NTP service
│
└── ise/
    ├── ISE_Overview.md
    ├── RADIUS_TACACS.md
    └── FortiGate_Integration.md
```


---

## 🧪 **7. Testing & Validation Performed**

✔ Inter-VLAN routing  
✔ Branch → HQ reachability  
✔ DMZ accessibility tests  
✔ DHCP lease distribution  
✔ AD authentication via ISE  
✔ VPN tunnel stability  
✔ HA failover test (FortiGate A-P)  
✔ L2 security enforcement (DAI, Snooping, Port Security)  
✔ Security policy filtering  
✔ Syslog/SNMP monitoring validation  

---

## 👥 **8. Team Members**

- Habib Wael Suleiman  
- Ahmed Yasser Aziz  
- Morcos Osama  
- Saeed Khaled  
- Amr Tarek  
- Ziad Mahfouz  

Supervised by:  
**Dr. Hussein Harb**  
Assisted by:  
**Eng. Elhussein Ahmed**

---

## 📄 **9. License**

This project is part of the **DEPI – Fortinet Cybersecurity Track** and is intended for educational and professional demonstration purposes.

---

##  **10. Feedback & Contributions**

Feel free to contribute improvements or suggestions to enhance the documentation or add additional automation scripts.

---

