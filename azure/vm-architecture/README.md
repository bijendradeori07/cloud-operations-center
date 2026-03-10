\# Azure VM Architecture – Cloud Operations Center



This directory documents the \*\*Azure Virtual Machine architecture\*\* implemented as part of the \*\*Cloud Operations Center\*\* project.



The setup reflects a \*\*real-world enterprise Azure environment\*\* with security, monitoring, backup, governance, and operational visibility.



---



\## Architecture Overview



The Azure implementation includes:



* &nbsp;Windows and Linux Virtual Machines
* Separate Resource Groups for workload isolation
* Virtual Network with subnets
* Network Security Groups attached at subnet level
* Role-Based Access Control (RBAC)
* Centralized monitoring and alerting
* Backup and recovery using Recovery Services Vault
* Operational access via PowerShell, SSH, and RDP
* Nginx web server hosted on Linux VM



This architecture is designed for \*\*operational readiness\*\*, not just deployment.



---



\## High-Level Components



|  Component  |            Description             |

|-------------|------------------------------------|

| Compute     | Windows and Linux Virtual Machines |

| Networking  | VNet, Subnets, NSGs                |

| Security    | RBAC, NSG rules                    |

| Monitoring  | Log Analytics, Alerts              |

| Backup      | Recovery Services Vault            |

| Operations  | PowerShell, SSH, RDP               |

| Application | Nginx on Linux VM                  |

|-------------|------------------------------------|





---





\## Documentation Structure



Each area of the architecture is documented separately for clarity.



|             File           |                Description              |

|----------------------------|-----------------------------------------|

| `azure-architecture.md`    | Overall Azure architecture design       |

| `overview.md`              | High-level VM deployment summary        |

| `compute.md`               | Virtual machine details                 |

| `networking.md`            | VNet, subnet, and NSG configuration     |

| `rbac.md`                  | Role-Based Access Control configuration |

| `monitoring.md`            | Log Analytics and alerts                |

| `backup-recovery.md`       | VM backup and recovery setup            |

| `nginx.md`                 | Nginx installation and validation       |

| `powershell-operations.md` | Operational commands and validation     |

| `troubleshooting.md`       | Known issues and fixes                  |

| `screenshots/`             | Redacted visual evidence                |

|----------------------------|-----------------------------------------|







---





\## Operational Characteristics



This Azure setup supports:



* Secure administrative access
* Controlled inbound and outbound traffic
* Proactive monitoring and alerting
* Disaster recovery preparedness
* Clear separation of duties
* Audit-friendly design





---





\## Audience



This documentation is intended for:



* Cloud Operations Engineers
* Cloud Operations Analyst
* DevOps Engineers (Operations-focused)
* SRE
* Technical interview reviewers





---





\## Relationship to Other Sections



* Jira tracks delivery and operations for this architecture
* GitHub serves as the source of documentation truth
* Monitoring alerts feed into ITSM workflows
* Changes are governed through change management













