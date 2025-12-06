#  DHCP Server

##  Overview
DHCP automatically assigns IP addresses, DNS, and gateway settings to all devices in HQ and Branch networks.

##  Purpose in the Project
- Central IP management  
- Automatic onboarding for VLANs and branch networks  
- Consistent IP/DNS/Gateway assignments  
- Reduces manual configuration  

##  Scopes Created
### HQ VLAN Scopes
- HR → 172.16.0.0/27  
- Sales → 172.16.0.32/27  
- Finance → 172.16.0.64/27  
- Media → 172.16.0.96/27  
- IT → 192.168.10.0/24  

### Branch VLAN Scopes
- HR → 172.17.0.0/27  
- Sales → 172.17.0.32/27  
- Finance → 172.17.0.64/27  
- Media → 172.17.0.96/27  
- IT → 192.168.11.0/24  

##  Testing
- Verified IP assignment per VLAN  
- Correct gateway & DNS options  
- Branch clients receive IP via VPN tunnel  

