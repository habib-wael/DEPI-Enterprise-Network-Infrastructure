#  DNS Server

##  Overview
DNS translates domain names into IP addresses, allowing devices to locate services such as AD, web servers, SMTP, FTP, and DMZ systems.

##  Purpose in the Project
- Provide name resolution for internal services  
- Support AD Domain Join (required service)  
- Resolve ISE, FortiGate, and server names  
- Provide DNS for DHCP clients in HQ & Branches  

##  Configuration Summary
- Zone Name: **corp.local**
- Reverse Lookup Zones created  
- A-records for:
  - DC01 (Domain Controller)
  - ISE Server
  - FortiGate
  - Web Server
  - FTP Server
  - Syslog Server
  - Branch Routers

##  Testing
- `nslookup` success from HQ & Branch  
- AD Join succeeded  
- DNS used by DHCP clients  
