# Architecture Overview
This documents describe the Azure Infrastructure architecture implemented as part of the **Cloud Operations Center** project.

The design follows **enterprises best practices** for networking, security, monitoring, backup and operations.

The architecture supports:

- Linux and Windows workloads
- Secure network isolation
- Centralized monitoring and alerting
- Backup and recovery
- Operational management using Powershell

## Architecture Components

The Azure environment consists of the following core components:
- Resource Groups ( workload separation)
- Virtual Network
- Subnets
- Network Security Groups (NSG)
- Virtual Machines (Linux \& Windows)
- Log Analytics Workspace
- Azure Monitor Alerts
- Recovery Services Vault
- Roled-Based Access Control (RBAC)

## Resource Group design

1. Workload Resource Groups
Separate resources groups were created to logically isolate workloads:

- Linux VM resource group
- Windows VM resource group

This separation allows:

- Independent lifecycle management
- Clear Ownership boundaries
- Reduced blast radius during changes

2. Shared Services Resource Group

A common resource group was created to host shared services:
- Log Analytics Workspace
- Recovery Services Vault

This follows an **enterprise-shared-service model **, avoiding duplication and simplifying operations.

## Networking Architecture

1. Virtual Network (VNet)
- A custom Virtual Network was created.
- Address space planned manually to support future expansion

2. Subnet Design
- Separate subnets were created for:
   - Linux VM
   - Windows VM

- This provides workload isolation and improved security level

3. Network Security Groups (NSG)
- NSGs were **associated at the subnet level** (not NIC level)
- This simplifies security management and aligns with Azure best practices


### Inbound rules
   - SSH(22) :  Restricted to admin IP
   - RDP(3389): Restricted to admin IP
   - HTTP(80) : Allowed for web access testing

## Compute Architecture

1. Linux Virtual Machine
- OS: Ubuntu LTS
- Access method: SSH(key-based authentication)
- Web Server: Nginx
- Used to validate:
       - Linux admin
       - Network Security
       - Web Traffic flow

2. Windows Virtual Machine
- OS: Windows Server
- Access method: RDP
- Managed using PowerShell
- Used to validate:
       - Windows admin
       - Powershell-based operations
       - Enterprise VM management scenarios


## Identity & Access Management (RBAC)

1. Azure RBAC was reviewed at:
- Subscription level
- Resource Group level
- Resource level
- Role inheritance behaviour was validated
- This helped understand permission boundaries and access control flow

RBAC awareness is critical for secure enterprise cloud operations.


## Monitoring & Observability

1. Log Analytics Workspace
- Central Log Analytics Workspace created in shared services resource group
- Both Linux Windows VMs connected to the workspace

2. Metrics & Logs Collected
- CPU Utilization
- VM heartbeat
- Performance Counter
- System logs

3. Alerts
-  Azure Monitor alerts were configured for :
                - VM down
                - High CPU Utilization

This enables **proactive monitoring** and faster incident detection

## Backup & Recovery Architecture

1. Recovery Services Vault
- RSV created in shared services resource group
- Both Linux and Windows VMs protected

2. Backup Configuration
- Scheduled backups enabled
- Retention policies enabled

This ensures:
- Data Protection
- Disaster recovery readiness
- Compliance with operational best practice

## Operations & Administration

1. PowerShell Operations
- PowerShell used as the primary operational tools
- Both VMs managed using PowerShell:
          - Windows VM via native PowerShell
          - Linux VM via SSH PowerShell

2. Operational Benefits
- Reduced dependency on Azure Portal
- CLI-driven operational mindset
- Foundation for automation and scripting

## Security Considerations

The architecture incorporate the following security practices:
- NSG applied at Subnet level
- Restricted administration access (SSH/RDP)
- RBAC scope awareness 
- Monitoring and alerting enabled
- Backup enabled for recovery scenarios

Sensitive identifiers are intentionally hidden in documentation and screenshots.

## Architecture Outcomes

This Azure Architecture demonstrates:
- Enterprise-style workload separation
- Secure network design
- Cross-platform VM operations
- Centralized monitoring and alerting
- Backup and recovery planning
- CloudOps-focused operational practices

## Summary

The Azure VM architecture implemented in this project reflects **real-world Cloud Operations design** simple lab setup.

It is suitable for demonstrating skill required for:
- Cloud Operations Engineer
- Cloud Operations Analyst
- DevOps Engineer (Operations-focused)
- Junior Site Reliability (SRE)
- Cloud Support Engineer (L2/L3)


This architecture forms a strong foundation for further automation, scaling and CI/CD integration.



