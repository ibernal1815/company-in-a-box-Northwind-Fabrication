# Environment Overview

## Purpose

This project documents a complete internal IT environment for a fictional mid sized company with approximately fifty employees. The environment is built and operated as if maintained by a first hire IT Systems Specialist who is still a student.

The focus is on practical, supportable IT operations under real hardware constraints rather than idealized enterprise designs.

## Company profile

The fictional company has approximately fifty employees across the following departments:

- IT
- Human Resources
- Finance
- Engineering
- Sales

Most employees use Windows 11 workstations and rely on centralized authentication and file storage.

## Domain information

- Internal domain name: northwind.local
- Domain type: single forest, single domain
- Time zone: Pacific Time (UTC-8)

A single domain is used to minimize administrative overhead and complexity.

## Core services provided

- Active Directory Domain Services
- DNS and DHCP
- Group based access control
- Departmental file shares
- Centralized logging
- Backups and recovery testing
- PowerShell based user onboarding and offboarding

## Hosting constraints

All systems are hosted on a single workstation using VMware Workstation Pro.

- Storage: 512GB NVMe
- Memory: 48GB RAM
- CPU: Intel i5-14400F

Resource allocation is intentionally conservative to maintain host stability.
