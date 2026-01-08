# Identity And Access

## Domain structure

- Domain: northwind.local
- Authentication source: Active Directory Domain Services
- Single domain model

## Organizational units

Top level OUs:

- Servers
- Workstations
  - Engineering
  - HR
  - Finance
  - Sales
- Users
  - Engineering
  - HR
  - Finance
  - Sales
- Groups

## Group model

Department groups:

- GG Engineering Users
- GG HR Users
- GG Finance Users
- GG Sales Users

File access groups:

- GG Engineering Share RW
- GG HR Share RW
- GG Finance Share RW
- GG Sales Share RW

Administrative groups are limited and documented separately.

## Least privilege approach

Users are assigned only to the groups required for their role. Direct permissions on resources are avoided.
