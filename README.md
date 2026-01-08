# Internal IT Environment Lab

This repository documents a complete internal IT environment built for a fictional mid sized company with approximately fifty employees. The environment is designed and maintained as if by a first hire IT Systems Specialist who is still a student, balancing best practices with realistic constraints and day to day operational needs.

The focus of this project is practical IT operations rather than theoretical or enterprise scale designs. Systems are built incrementally, validated as they are added, and documented with the assumption that another administrator or instructor may rely on this documentation to understand, operate, or recover the environment.

## Environment scope

The lab environment supports the following core functions:

- Identity and access management using Active Directory
- Group based permissions and least privilege access
- Department based file services
- Basic network segmentation
- Centralized logging and monitoring
- Backups with documented recovery testing
- User onboarding and offboarding automation using PowerShell

The scope is intentionally limited to remain supportable by a single administrator.

## Host system constraints

All virtual machines run on a single workstation using VMware Workstation Pro. Design decisions explicitly account for these limits.

Storage: 512GB NVMe  
Memory: 48GB RAM  
CPU: Intel i5 14400F  

Services are consolidated where appropriate, and unnecessary components are avoided to prevent over allocation and instability.

## Design approach

This project prioritizes clarity, reliability, and recoverability over complexity.

- Systems are built in phases rather than all at once
- Each major component is validated before moving forward
- Trade offs and limitations are documented honestly
- Automation scripts favor readability and safe failure
- Recovery procedures are treated as first class documentation

Mistakes are expected and planned for through backups, logging, and clear operational notes.

## Repository structure

```text
Documentation/
  Environment Overview/
  Network Design/
  Server Builds/
  Identity And Access/
  File Services/
  Logging And Monitoring/
  Backups And Recovery/
  Change Log/

Scripts/
  Onboarding/
  Offboarding/
  Shared Functions/

Configs/
  GPO Backups/
  DHCP Exports/

Diagrams/
Evidence/
```

This is a long running project. Features are added gradually, and documentation is updated alongside implementation. Changes are tracked in the change log with context and reasoning.

