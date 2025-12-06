#  IIS Web Server

##  Overview
IIS hosts internal websites used for enterprise services.

##  Purpose in the Project
- Host internal test pages  
- Validate DMZ zone traffic restrictions  
- Demonstrate secure web publishing through FortiGate  

##  Configuration
- HTTP & HTTPS enabled  
- Certificate from CA applied  
- Runs inside DMZ (10.20.20.0/27)  

##  Testing
- Access from HR/Sales/Finance based on firewall policy  
- Access denied from unauthorized VLANs  

