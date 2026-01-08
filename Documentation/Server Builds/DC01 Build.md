# DC01 Build

## Purpose

DC01 is the primary domain controller for the northwind.local domain. It provides Active Directory Domain Services, DNS, and DHCP.

## Prerequisites

- VMware Workstation Pro installed on host
- Windows Server 2022 ISO available
- VMnet10 (Server Network) configured
- Static IP plan defined

## Virtual machine configuration

- VM name: DC01
- OS: Windows Server 2022 Standard
- vCPU: 2
- Memory: 6GB
- Disk: 80GB
- Network: VMnet10

## Network configuration

- IP address: 10.10.10.10
- Subnet mask: 255.255.255.0
- Default gateway: 10.10.10.1
- Preferred DNS: 10.10.10.10

## Operating system configuration

- Hostname: DC01
- Time zone: Pacific Time
- Windows updates applied before role installation

## Role installation

Install the following roles:
- Active Directory Domain Services
- DNS Server
- DHCP Server

## Domain configuration

- New forest and domain: northwind.local
- Forest functional level: Windows Server 2022
- Domain functional level: Windows Server 2022

## DHCP configuration

- Scope: 10.10.20.0/24
- Range: 10.10.20.100–10.10.20.199
- DNS server: 10.10.10.10
- Default gateway: 10.10.20.1

## Validation

- Domain controller appears in Active Directory Users and Computers
- DNS zone northwind.local exists
- DHCP scope is active
- Test client receives an IP address

## Notes

Any deviations from this build should be documented in the change log.
