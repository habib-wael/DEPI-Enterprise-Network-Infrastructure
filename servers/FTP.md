#  FTP Server

##  Overview
Provides internal file transfer service for testing security policies.

##  Purpose
- Validate DMZ firewall restrictions  
- Provide test service for branch-to-HQ access  
- Demonstrate control via ACL & FortiGate policies  

##  Settings
- Passive mode configured  
- Authentication through local users  
- Port 21 allowed only from permitted VLANs  

##  Testing
- Allowed from IT only  
- Blocked from HR / Sales etc.  

