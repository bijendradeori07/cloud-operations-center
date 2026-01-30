Md







\# Root Architecture – Cloud Operations Center (Multi-Cloud)





\## Architecture Purpose



This document defines the \*\*high-level architecture\*\* of the Cloud Operations Center (COC).



The goal of this architecture is to demonstrate \*\*how cloud environments are operated end-to-end\*\* across \*\*Azure and AWS\*\*, using \*\*centralized operations, monitoring, ITSM workflows, and governance\*\*.



This is an \*\*operations-first architecture\*\*, not a deployment-only design.



---



\## Architectural Scope



The architecture covers:



* Multi-cloud infrastructure (Azure + AWS)
* Compute, networking, security, monitoring, and backup
* Centralized operations and governance
* ITSM workflows using Jira
* Evidence-driven documentation using GitHub



\*\*Out of scope:\*\*

* Application development
* CI/CD pipelines
* Infrastructure as Code (future enhancement)



---



\## High-Level Architecture Overview





+--------------------------------------------------------------------+

|                     Cloud Operations Center                        |

+--------------------------------------------------------------------+

|                                                                    |

|   +---------------------+     +---------------------------------+  |

|   |   Jira Software     |     |  Jira Service Management        |  |

|   |   (Delivery)        |     |  (ITSM / Operations)            |  |

|   |                     |     |                                 |  |

|   | Epics / Stories     |     | Incidents / Changes             |  |

|   | Tasks / Subtasks    |     | Problems / SLAs / RCA           |  |

|   +----------+----------+     +---------------+-----------------+  |

|              \\                                /                    |

|               \\                              /                     |

|                +----------------------------+                      |

|                |    Operational Governance  |                      |

|                |  ITIL • SLAs • Traceability|                      |

|                +-------------+--------------+                      |

|                              |                                     |

|        +---------------------v------------------------+            |

|        |          Monitoring \& Observability          |            |

|        |   Azure Monitor | Log Analytics | Alerts |   |            |

|        |             |  AWS CloudWatch  |             |            |

|        +---------------------+------------------------+            |

|                              |                                     |

+------------------------------+-------------------------------------+

&nbsp;                              |

&nbsp;              +---------------+-------------------+

&nbsp;              |                                   |

&nbsp;    +---------v---------+               +---------v---------+

&nbsp;    |      Azure        |               |        AWS        |

&nbsp;    |-------------------|               |-------------------|

&nbsp;    | Linux VM (Ubuntu) |               | EC2 Instance      |

&nbsp;    | Windows Server VM |               | Nginx Web Server  |

&nbsp;    | VNet \& Subnets    |               | Security Groups   |

&nbsp;    | NSG (Subnet)      |               | SSH Access        |

&nbsp;    | Backup (RSV)      |               | VM Disks(EBS)     |

&nbsp;    | Diagnostics Logs  |               |                   |

&nbsp;    | Boot Diagnostics  |               |                   |

&nbsp;    +-------------------+               +-------------------+











---



\## Core Architectural Pillars



\### Multi-Cloud Operations



* Azure and AWS are operated \*\*in parallel\*\*
* Each cloud has independent infrastructure
* Operations, Monitoring, and ITSM are \*\*centralized\*\*
* Cloud-specific details are isolated under their respective directories



---



\### Compute Layer



\*\*Azure (Implemented)\*\*

* Ubuntu Linux VM
* Windows Server VM
* Operated using PowerShell and SSH



\*\*AWS (Implemented)\*\*

* EC2 instances
* Linux-based workloads
* Nginx web server



---



\### Storage Layer



Storage services are used in both cloud platforms to support

diagnostics, logging, backups, and operational data.



\*\*Azure Storage (Implemented)\*\*



\- Storage Accounts used for:

&nbsp; - Boot diagnostics

&nbsp; - VM diagnostics and logs

&nbsp; - Monitoring data integration

\- Integrated with Azure Monitor and Log Analytics

\- Storage scoped and governed via Resource Groups

\- Access controlled using Azure RBAC



\*\*AWS Storage (Implemented)\*\*



\- Amazon EBS volumes attached to EC2 instances

\- Used for:

&nbsp; - Operating system disks

&nbsp; - Application data (Nginx)

\- Storage access governed by instance-level permissions





\### Networking \& Security



\*\*Azure (Implemented)\*\*

* Custom Virtual Network (VNet)
* Separate subnets for workloads
* Network Security Groups (NSG) applied at \*\*subnet level\*\*
* Restricted SSH and RDP access
* RBAC scope validation



\*\*AWS (Implemented)\*\*

* Security Groups with least-privilege rules
* SSH access restricted via key-based authentication



---



\### Monitoring \& Observability



\*\*Azure (Implemented)\*\*

* Azure Monitor
* Log Analytics Workspace
* VM Performance metrics
* Availability metrics
* Alert rules for:

&nbsp; - VM down

&nbsp; - High CPU utilization

* Alert validation and testing performed
* Centralized Monitoring Resource groups
* Diagnosed logs stored in Azure Storage Accounts
* VM boot diagnostics retained for troubleshooting



\*\*AWS (Implemented)\*\*

* Amazon CloudWatch
* EC2 instance metrics
* CloudWatch Alarms

&nbsp;  - Instance status check failure

&nbsp;  - High CPU utilization

* CloudWatch Logs for system and application logs
* SNS-based alert notification





---



\### Backup \& Recovery



\*\*Azure (Implemented)\*\*

* Recovery Services Vault
* Backup policies and retention rules
* Restore readiness validated
* Backup resources separated into dedicated/shared resource groups



\*\*AWS (Planned /Future Scope)\*\*



* AWS Backup (centralized backup service)
* EC2 snapshot-based backups
* Backup plan and retention policies
* Cross-Regions or cross-account backup (future enhancements)





> Note: AWS Backup and recovery is intentionally not implemented yet to maintain focused on Azure operational depth in the current phase.



---



\## ITSM \& Operational Governance Architecture



\### Jira Software (Delivery Layer)



Used to track \*\*infrastructure delivery work\*\*, including:



* Epics
* Stories
* Tasks
* Subtasks



Delivery work is split by cloud:

* Azure delivery
* AWS delivery



This layer answers:  

\*\* “ What is being built or changed ?” \*\*



---



\### Jira Service Management (Operations Layer)



Used for \*\*day-2 operations\*\*, including:



* Incident Management
* Problem Management
* Change Management
* Service Requests
* SLA enforcement



ITSM workflows are implemented separately for:

* Azure operations
* AWS operations



This layer answers:  

\*\* “ How is the environment supported and operated ?” \*\*



---



\## Documentation \& Evidence Architecture



* GitHub is used as the \*\*single source of truth\*\*
* Architecture, operations, and workflows are documented using Markdown
* Screenshots are stored as evidence for:

&nbsp; - Infrastructure

&nbsp; - Monitoring

&nbsp; - Security

&nbsp; - ITSM workflows

* Sensitive data is intentionally masked



Documentation is structured to be:

* Auditable
* Interview-ready
* Scalable



---



\## Design Principles Applied



* Operations-first mindset
* Least-privilege security
* Separation of concerns
* Centralized monitoring
* ITIL-aligned processes
* Clear traceability between infrastructure and ITSM records



---



\## Intended Audience



This architecture is designed for:



* Cloud Operations Engineers
* Cloud Operations Analysts
* DevOps Engineers (operations-focused)
* Site Reliability Engineers (Junior–Mid)
* Cloud Support Engineers (L2 / L3)



---



\## Architecture Evolution (Future Scope)



Potential future enhancements (not implemented yet):



* AWS Backup and Recovery implementation
* Infrastructure as Code (Terraform / Bicep)
* CI/CD integration
* Automated remediation
* Cost optimization dashboards
* Kubernetes-based workload orchestration



Kubernetes will introduced to demonstrate:



* Containerized workload operations
* Node-level monitoring and alerting
* Pod and service availability tracking
* Kubernetes incident and change handling Jira
* Operational visibility across VM-based and container-based platforms



These enhancements are intentionally excluded from the current implementations to keep the scope \*\*focused on VM-based cloud operations and ITSM fundamentals.\*\*



---



\## Summary



This root architecture represents a \*\*realistic Cloud Operations Center\*\*,

showing how cloud platforms are \*\*operated, governed, monitored, and supported\*\*

in professional environments — not just deployed.



It connects:

* Infrastructure
* Monitoring
* Security
* Backup
* ITSM
* Documentation



into a single, coherent operational system.





















