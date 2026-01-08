# Server Inventory

## Server list

DC01  
- Role: Domain Controller, DNS, DHCP  
- OS: Windows Server 2022  
- CPU: 2 vCPU  
- Memory: 6GB RAM  
- Storage: 80GB  

FS01  
- Role: File Services  
- OS: Windows Server 2022  
- CPU: 2 vCPU  
- Memory: 8GB RAM  
- Storage: 80GB OS + 150GB data disk  

LOG01  
- Role: Centralized logging  
- OS: Ubuntu Server  
- CPU: 2 vCPU  
- Memory: 4GB RAM  
- Storage: 80GB  

BKP01  
- Role: Backup repository  
- OS: Ubuntu Server  
- CPU: 2 vCPU  
- Memory: 4GB RAM  
- Storage: 150GB  

## Allocation rationale

Resource allocations are intentionally modest to avoid overcommitting the host system while still providing stable service performance.
