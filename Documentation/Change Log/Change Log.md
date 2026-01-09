# Change Log

This document records significant design and implementation decisions for the internal IT environment. Entries reflect completed milestones that materially affect how the environment is built, operated, or understood.

## 2026-01-07

Finalized baseline environment design and documentation structure.

- Defined project scope, constraints, and guiding principles
- Established repository structure for documentation, scripts, configurations, and evidence
- Created and refined the primary README to describe project intent and organization

## 2026-01-07

Defined core environment architecture and constraints.

- Confirmed single-host VMware Workstation Pro deployment model
- Documented host hardware limits and resource allocation strategy
- Finalized approach favoring simplicity and service consolidation

## 2026-01-07

Established domain, identity, and access model.

- Selected internal domain name northwind.local
- Defined single-domain Active Directory model
- Documented OU structure for users, workstations, servers, and groups
- Defined department-based security group naming and usage
- Documented least privilege access approach

## 2026-01-07

Finalized network design and IP addressing.

- Defined Server Network (VMnet10) using 10.10.10.0/24
- Defined Client Network (VMnet20) using 10.10.20.0/24
- Assigned static IP addresses for all planned servers
- Defined DHCP scope for client systems
- Documented routing and access assumptions

## 2026-01-08

Defined server roles and resource allocations.

- Identified four core servers: DC01, FS01, LOG01, and BKP01
- Documented operating systems, roles, and responsibilities for each server
- Finalized conservative CPU, memory, and storage allocations to respect host limits

## 2026-01-08

Completed detailed server build runbooks.

- Created DC01 build document covering AD DS, DNS, and DHCP configuration
- Created FS01 build document covering file services and permissions model
- Created LOG01 build document covering centralized logging approach
- Created BKP01 build document covering backup storage and recovery testing

## 2026-01-08

Built DC01 and established core identity and network services.

- Created DC01 virtual machine in VMware Workstation Pro
- Installed Windows Server 2022 Standard
- Applied initial operating system updates
- Configured static IP address 10.10.10.10 on the Server Network (VMnet10)
- Promoted DC01 to a domain controller for the northwind.local domain
- Installed and configured DNS services
- Installed, authorized, and configured DHCP
- Created and activated DHCP scope for the Client Network (10.10.20.100–10.10.20.199)

DC01 now provides Active Directory, DNS, and DHCP services for the environment and serves as the foundational infrastructure component.


These runbooks serve as the authoritative reference for building and rebuilding the environment.
