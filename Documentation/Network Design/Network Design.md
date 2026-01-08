# Network Design

## Overview

The network design provides basic segmentation between servers and client systems while remaining simple enough to manage without dedicated networking hardware.

## VMware virtual networks

Two internal networks are used:

- Server network  
  VMware network: VMnet10  
  Subnet: 10.10.10.0/24  

- Client network  
  VMware network: VMnet20  
  Subnet: 10.10.20.0/24  

Both networks use NAT for outbound internet access when required.

## IP addressing

### Server network (10.10.10.0/24)

- DC01: 10.10.10.10
- FS01: 10.10.10.20
- LOG01: 10.10.10.30
- BKP01: 10.10.10.40

Server addresses are statically assigned to simplify troubleshooting and documentation.

### Client network (10.10.20.0/24)

- DHCP scope: 10.10.20.100 – 10.10.20.199
- Gateway: 10.10.20.1
- DNS: 10.10.10.10

## Routing and access

Inter-network communication is allowed for required services such as authentication, DNS, file access, and logging. Advanced firewall segmentation is intentionally out of scope for this lab.
