#  NTP Server

##  Overview
Provides time synchronization to all devices (AD, ISE, switches, firewall).

##  Purpose
- Ensure accurate logs  
- Required for AD + ISE authentication  
- Required for certificates validation  

##  Config
- Windows Server configured as NTP source  
- Network devices point to server IP  

##  Testing
- `show clock` matches server time  

