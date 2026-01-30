Md





\# Cloud Operations Center (Multi-Cloud)



A simulated **Cloud Operations Center (COC)** designed to mirror real-world, production-style cloud operations across \*\*Azure and AWS\*\*, focusing on \*\*monitoring, security, ITSM SLA and Operational governance\*\*.



This repository demonstrates not just cloud deployment, but \*end-to-end cloud operations\*\* using \*\*Jira Software, Jira Service Management, and GitHub\*\*.





---



\## 🔍 Project Overview



The Cloud Operations Center showcases how modern cloud environments are:



* Deployed
* Secured
* Monitored
* Operated
* Supported using ITIL-aligned processes



The project follows \*\*real CloudOps / SRE practices\*\*, not lab-only setups.



---



\## ☁️ Cloud Platforms Covered



\### Microsoft Azure



* Linux VM (Ubuntu)
* Windows Server VM
* Custom Virtual Network (VNet)
* Separate subnets for workloads
* Network Security Groups (NSG) at Subnet level
* Azure Monitor
* Alert Rules(VM down, high CPU usage)
* Recovery Services Vault (Backup, Backup Policy, Retention)
* Storage Account (Diagnostics \& Logs)
* RBAC scope awareness
* Powershell-based operations



\### Amazon Web Services (AWS)



* EC2
* Security Groups
* Storage
* Nginx Web Server
* SSH access with key-based authentication



---





\## 🏗️ Architecture Highlights



* Multi-resource-group design
* Shared service resource group (Monitoring \& Backup)
* Least-Privilege network security
* Centralized monitoring
* Backup \& Recovery readiness
* Cross-platform operations (Windows \& Linux)
* Multi-cloud visibility (Azure + AWS)



---





\## 🛠️ Operations \& Tooling



* \*\*Powershell\*\* for VM Operations
* \*\*SSH\*\* for Linux administration
* \*\*Azure Portal \& CLI
* \*\*AWS Management Console\*\*
* \*\*GitHub\*\* for documentation \& evidence
* \*\*Jira\*\* for delivery \& ITSM workflows





---





\## 📊 Monitoring, Alerts \& Backup





\### Monitoring

* Azure Monitor
* Log Analytics Workspace
* Performance \& availability metrics



\### Alerts

* VM availability ( VM down)
* CPU utilization threshold
* Alerts validation and testing



\### Backup

* Recovery Services Vault
* Scheduled backups
* Retention Policies
* Restore readiness





\## 🔐 Security \& Governance

* NSG rules applied at subnet level
* Restricted SSH and RDP access
* RBAC scope validation
* Secure storage configuration
* Sensitive data masked in screenshots



---



\## 🧾 ITSM \& Jira Integration



This project integrates \*\*Jira Software\*\* and \*\*Jira Service Management\*\* to reflect real operational workflows





\### Jira Software (Delivery)



* Incident Management
* Problem Management
* Change Management
* Service Management
* SLA definitions
* Multi-cloud Incident sources (Azure+ AWS)



---

\## ⏱️ Service Level Agreements(SLA)



SLA are defined for:



* Incidents (response \& resolution)
* Changes (approval \& implementation)
* Problems (RCA \& permanent fix)
* Service request(fulfillment time)



All SLAs follow \*\*ITIL best practices and documented centrally.



---


```
\## 📁 Repository Structure





      cloud-operations-center/
        │
        ├──── .gitignore
        │
        ├──── README.md
        │    
        ├──── root-architecture.md
        │  
        │
        ├──── aws/
        │        └───── ec2
        │                 ├────── aws-architecture.md
        │                 ├────── README.md 
        │                 ├────── steps.md
        │                 ├────── security-groups
        │                 └────── screenshots/
        │                              ├────── ec2-overview.png
        │                              ├────── security-group-rules.png
        │                              └────── nginx-page.png
        │   
        │ 
        │ 
        │  
        │  
        │     
        │      
        │     
        │  
        │
        ├──── azure/
        │        └───── vm-architecture
        │                 ├────── azure-architecture.md
        │                 ├────── README.md
        │                 ├────── overview.md
        │                 ├────── compute.md
        │                 ├────── networking.md
        │                 ├────── rbac.md
        │                 ├────── monitoring.md
        │                 ├────── back-recovery.md
        │                 ├────── nginx.md
        │                 ├────── powershell-operations.md
        │                 └────── screenshots/
        │                              ├────── vm-linux-overview.png
        │                              ├────── vm-windows-overview.png
        │                              ├────── resource-groups-overview.png
        │                              ├────── nsg-inbound-rules.png
        │                              ├────── 
        │                              ├──────
        │                              ├────── dcr-log-analytics-visualizer.png
        │                              ├────── backup-rsv.png
        │                              ├────── backup-enhanced-policies.png
        │                              ├────── ssh-login-ubuntu-using-key.png
        │                              ├────── windows-powershell-disk-network-validation.png
        │                              ├────── windows-boot-diagnostics.png
        │                              └──────
        │        
        │   
        │ 
        │     
        │     
        │                                                          
        ├──── jira/
        │        │                 
        │        ├────── README.md
        │        │                 
        │        ├────── jira-architecture.md
        │        │        
        │        │        
        │        ├────── workflow.md       
        │        │   
        │        │        
        │        │  
        │        ├────── jira-software/      
        │        │        │
        │        │        ├────── jsw-aws/
        │        │        │           ├────── jsw-aws-architecture.md
        │        │        │           │         
        │        │        │           ├────── README.md        
        │        │        │           │
        │        │        │           │
        │        │        │           │
        │        │        │           ├────── epics/
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────  
        │        │        │           │           └──────
        │        │        │           │
        │        │        │           │
        │        │        │           │
        │        │        │           ├────── stories/
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           ├──────
        │        │        │           │           └──────
        │        │        │           │          
        │        │        │           │          
        │        │        │           │  
        │        │        │           │
        │        │        │           ├────── tasks/  
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          ├──────
        │        │        │           │          └──────
        │        │        │           │
        │        │        │           │
        │        │        │           │
        │        │        │           │  
        │        │        │           └────── subtasks/
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       ├──────
        │        │        │                       └──────
        │        │        │
        │        │        │
        │        │        │
        │        │        │
        │        │        │
        │        │        └────── jsw-azure/
        │        │                    │
        │        │                    ├────── jsw-azure-architecture.md
        │        │                    │         
        │        │                    ├────── README.md        
        │        │                    │
        │        │                    │
        │        │                    ├────── epics/
        │        │                    │         ├────── azure-infrastructure-deployment.md
        │        │                    │         └────── azure-security-monitoring-backup.md
        │        │                    │        
        │        │                    │            
        │        │                    │           
        │        │                    │         
        │        │                    ├────── stories/ 
        │        │                    │         ├────── azure-resource-group-standards.md
        │        │                    │         ├────── deploy-linux-vm.md
        │        │                    │         ├────── deploy-windows-vm.md
        │        │                    │         ├────── azure-network-architecture.md
        │        │                    │         ├────── azure-network-security.md
        │        │                    │         ├────── azure-vm-backup.md
        │        │                    │         ├────── azure-monitoring-log-analytics.md
        │        │                    │         ├────── azure-vm-alerts.md
        │        │                    │         ├────── azure-storage-account.md
        │        │                    │         └────── boot-diagnostics.md
        │        │                    │         
        │        │                    │        
        │        │                    │         
        │        │                    ├────── tasks/      
        │        │                    │         ├────── azure-resource-group-standards-tasks.md
        │        │                    │         ├────── deploy-linux-vm-tasks.md
        │        │                    │         ├────── deploy-windows-vm-tasks.md
        │        │                    │         ├────── azure-network-architecture-tasks.md
        │        │                    │         ├────── azure-network-security-tasks.md
        │        │                    │         ├────── azure-vm-backup-tasks.md
        │        │                    │         ├────── azure-monitoring-log-analytics-tasks.md
        │        │                    │         ├────── azure-vm-alerts-tasks.md
        │        │                    │         ├────── azure-storage-account-tasks.md
        │        │                    │         └────── boot-diagnostics-tasks.md
        │        │                    │      
        │        │                    │         
        │        │                    │         
        │        │                    │         
        │        │                    │                  
        │        │                    └────── subtasks
        │        │                              ├────── azure-resource-group-standards-subtasks.md
        │        │                              ├────── deploy-linux-vm-subtasks.md
        │        │                              ├────── deploy-windows-vm-subtasks.md
        │        │                              ├────── azure-network-architecture-subtasks.md
        │        │                              ├────── azure-network-security-subtasks.md
        │        │                              ├────── azure-vm-backup-subtasks.md
        │        │                              ├────── azure-monitoring-log-analytics-subtasks.md
        │        │                              ├────── azure-vm-alerts-subtasks.md
        │        │                              ├────── azure-storage-account-subtasks.md
        │        │                              └────── boot-diagnostics-subtasks.md
        │        │        
        │        │        
        │        │        
        │        │        
        │        ├────── jira-service-management/
        │        │                   │
        │        │                   ├────── jsm-aws/      
        │        │                   │         ├────── jsm-aws-architecture.md
        │        │                   │         ├────── README.md
        │        │                   │         ├────── incidents.md
        │        │                   │         ├────── changes.md
        │        │                   │         ├────── problems.md
        │        │                   │         ├────── service-requests.md
        │        │                   │         ├────── sla.md
        │        │                   │         └────── itsm-flow.png
        │        │                   │ 
        │        │                   │         
        │        │                   │        
        │        │                   │
        │        │                   │
        │        │                   │         
        │        │                   └────── jsm-azure/         
        │        │                           ├────── jsm-azure-architecture.md
        │        │                           ├────── README.md
        │        │                           ├────── incidents.md
        │        │                           ├────── changes.md
        │        │                           ├────── problems.md
        │        │                           ├────── service-request.md
        │        │                           ├────── sla.md
        │        │                           └────── itsm-flow.md
        │        │                        
        │        │                        
        │        │                     
        │        └────── screenshots/
        │                            ├────── jira-board.png
        │                            ├────── 
        │                            ├────── 
        │                            ├────── 
        │                            └────── 
        │                  
        │   
        │   
        └─── diagrams/
                 ├────── README.md
                 ├────── root-architecture.png
                 ├────── azure-architecture.png
                 ├────── aws-architecture.png
                 ├────── jira-hierarchy-epic-story-tasks-subtasks
                 └────── jira-cloudops-integration.png


```









\## 🎯 Key Outcomes



* Gained hands-on experience operating multi-cloud environments (Azure + AWS), including provisioning, securing, monitoring and maintaining Linux and Windows workloads.
* Implemented production-style cloud operations, covering incident management, problem analysis, change control, and service request handling Jira Software and Jira Service Management.
* Designed and operated secure network architecture, including VNets, Subnets and subnet-level NSGs, with least-privilege access and RBAC awareness.
* Built and validated end-to-end monitoring and alerting, integrating Azure Monitor, Log Analytics, and AWS CloudWatch to detect availability and performance issues.
* Established backup and recovery readiness, including Recovery Services Vault configuration, backup policies, retention planning and restore validation.
* Applied ITI-aligned SLAs for incidents, problems, changes and service request ensuring predictable response, approval and resolution timelines.
* Performed cross-platform operations using PowerShell and SSH, managing both Windows and Linux systems through command-line-driven workflows.
* Developed professional operations documentation, including architecture, Jira work item hierarchies, SLA definitions, and security-aware screenshots suitable for audit and interviews



\## 👔 Target Roles



* Cloud Operations Engineer
* Cloud Operations Analyst
* DevOps Engineer (Operations-focused)
* Junior Site Reliability Engineer(SRE)
* Cloud Support Engineer (L2/L3)





\## Disclaimer⚠️



This is a simulated Cloud Operations Center created for learning, demonstration and portfolio purposes.

No production customer data is used. All sensitive identifiers are masked.





\## Final Note📌



This is a repository demonstrate how cloud infrastructure is operated in real-world environments, not just deployed.


## Author 
Bijendra Kumar Deori