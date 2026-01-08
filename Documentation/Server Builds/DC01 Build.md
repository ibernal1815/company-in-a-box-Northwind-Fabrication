# DC01 Build

## Purpose

DC01 is the primary domain controller for the northwind.local domain. It provides Active Directory Domain Services, DNS, and DHCP for the environment.

This server forms the foundation for all identity, authentication, and name resolution services.

## Prerequisites

- VMware Workstation Pro installed on host
- Windows Server 2022 Standard ISO available
- VMnet10 (Server Network) configured
- IP addressing plan finalized

## Virtual machine configuration

- VM name: DC01
- Operating system: Windows Server 2022 Standard
- vCPU: 2
- Memory: 6 GB
- Disk: 60 GB
- Network adapter: VMnet10

## Network configuration

- IP address: 10.10.10.10
- Subnet mask: 255.255.255.0
- Default gateway: 10.10.10.1
- Preferred DNS server: 10.10.10.10

## Operating system configuration

- Computer name: DC01
- Time zone: Pacific Time
- Windows updates installed prior to role configuration

## Role installation

Install the following roles:
- Active Directory Domain Services
- DNS Server
- DHCP Server

## Domain configuration

- Create a new forest
- Domain name: northwind.local
- Forest functional level: Windows Server 2022
- Domain functional level: Windows Server 2022

## DHCP configuration

- DHCP scope: Client Network
- Network: 10.10.20.0/24
- Address range: 10.10.20.100 to 10.10.20.199
- Default gateway: 10.10.20.1
- DNS server: 10.10.10.10

## Validation

- Domain controller appears in Active Directory Users and Computers
- DNS forward lookup zone for northwind.local exists
- DHCP scope is active
- Test client receives an IP address and resolves DNS

## Notes

DC01 should not host additional roles beyond those defined here.
