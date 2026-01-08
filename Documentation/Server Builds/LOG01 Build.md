# LOG01 Build

## Purpose

LOG01 provides centralized log collection for servers and selected client systems. The logging solution prioritizes visibility and reliability over advanced analytics.

## Prerequisites

- DC01 operational
- Network connectivity to Server and Client networks
- Ubuntu Server ISO available

## Virtual machine configuration

- VM name: LOG01
- Operating system: Ubuntu Server LTS
- vCPU: 2
- Memory: 4 GB
- Disk: 80 GB
- Network adapter: VMnet10

## Network configuration

- IP address: 10.10.10.30
- Subnet mask: 255.255.255.0
- Default gateway: 10.10.10.1
- DNS server: 10.10.10.10

## Operating system configuration

- Hostname: LOG01
- Time zone: Pacific Time
- Automatic security updates enabled

## Logging configuration

- Central log service installed and configured
- Servers forward system and security logs
- Selected clients forward security related events

## Retention

- Logs retained for approximately 30 days
- Older logs rotated to conserve storage

## Validation

- Test events appear in centralized logs
- Timestamps and source systems are accurate

## Notes

LOG01 is not used for alerting or automated response.
