# 🏢 Active Directory Domain Services (AD DS)

## 📌 Overview
Active Directory is the central identity management system in the enterprise network.  
It stores user accounts, groups, computers, and policies, and provides authentication for all internal systems.

## 🎯 Purpose in the Project
- Authenticate users across HQ and Branches  
- Provide centralized identity for Cisco ISE  
- Manage domain computers  
- Apply Group Policies (GPO) for security  
- Integrate with FortiGate through FSSO  

## 🧱 AD Structure
- Domain Name: **corp.local**
- Organizational Units:
  - HQ Departments (HR, Sales, Finance, Media, IT)
  - Branch Departments
  - Servers
  - Admin Accounts

## 🔗 Integrations
- Cisco ISE (RADIUS, TACACS+)  
- FortiGate FSSO for identity-based firewall policies  
- DNS + DHCP  
- Windows login for clients

## 🧪 Validation
- Users successfully authenticated  
- Domain join tested  
- ISE reads AD groups correctly  
- Firewall identities detected via FSSO  

