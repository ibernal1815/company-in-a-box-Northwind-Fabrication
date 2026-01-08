# Internal IT Environment Lab

This repository documents a complete internal IT environment built for a fictional mid sized company with approximately fifty employees. The environment is designed and maintained as if by a first hire IT Systems Specialist who is still a student, balancing best practices with realistic constraints and day to day operational needs.

The goal of this project is to demonstrate practical IT operations rather than idealized or enterprise scale designs. All systems are built incrementally, validated as they are added, and documented with the assumption that another administrator may need to understand, operate, or recover the environment.

## Environment scope

The lab supports the following core functions:

- Identity and access management using Active Directory
- Group based permissions and least privilege access
- File services for multiple departments
- Basic network segmentation
- Centralized logging and monitoring
- Backups and documented recovery testing
- User onboarding and offboarding automation using PowerShell

The environment is intentionally limited in scope to remain supportable by a single administrator.

## Host system constraints

All virtual machines run on a single workstation using VMware Workstation Pro. Design decisions explicitly account for these limits.

- Storage: 512GB NVMe
- Memory: 48GB RAM
- CPU: Intel i5 14400F

Services are consolidated where appropriate, and unnecessary components are avoided to prevent over allocation and instability.

## Design approach

This project favors clarity, reliability, and recoverability over complexity.

- Systems are built in phases rather than all at once
- Each major component is validated before moving forward
- Trade offs and limitations are documented honestly
- Automation scripts prioritize readability and safe failure
- Recovery procedures are treated as first class documentation

Mistakes are expected and accounted for through backups, logging, and clear operational notes.

## Repository structure

- Documentation  
  Design decisions, build steps, and operational procedures
- Scripts  
  PowerShell scripts for onboarding, offboarding, and shared functions
- Configs  
  Exported configurations such as GPO backups and DHCP settings
- Diagrams  
  Network and system diagrams
- Evidence  
  Screenshots and results from testing and recovery exercises

## Intended audience

This repository is written for:
- Instructors evaluating applied IT skills
- Entry level and junior IT professionals
- Administrators looking for a realistic small environment reference

The documentation assumes basic familiarity with Windows Server, Active Directory, and PowerShell, but avoids unnecessary jargon where possible.

## Project status

This is a long running project. Features are added gradually, and documentation is updated alongside implementation. Changes are tracked in the change log with context and reasoning.

