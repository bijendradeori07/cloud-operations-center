Md





\# Jira - Cloud Operations Management



This section documents how \*\*Jira\*\* is used as the central system for \*\*planning , tracking and operating cloud infrastructure\*\* in this project.



Jira is used as for both:

* \*\*Delivery and implementation tracking\*\* 
* \*\*Operational and IT service management (ITSM)\*\*



The setup reflects how Jira is used in real world \*\*Cloud Operations, DevOps(operation-focused) and SRE environments\*\*.



---



\## Jira Usage Overview



Jira is implemented using two distinct applications:



|    Jira Application     |                Purpose                     |

|-------------------------|--------------------------------------------|

| Jira Software           | Planning and tracking delivery work        |

| Jira Service Management | Handling Operational support and incidents |

|-------------------------|--------------------------------------------|





Each application serves a different role but operates on the same cloud infrastructure.



---



\## Jira Software



Jira Software is used to manage \*\*planned work\*\*, including:



* Cloud Architecture implementation
* Azure and AWS infrastructure setup
* Monitoring and Backup configuration
* Documentation and GitHub Updates



Work is organized using:

* Epics
* Stories
* Tasks
* Subtasks



See 📁: `jira-software/`



--- 



\## Jira Service Management 



Jira Service Management is used for \*\*run-time operations\*\*, including:

* Incident handling
* Problem handling
* Change Management
* Service Requests
* SLA Tracking



This reflects an \*\*ITIL-aligned operational model\*\*



See 📁: `jira-service-management/`



---



\## Integration Context



Jira is conceptually integrated with:



* Azure Monitor and Log Analytics alerts
* AWS EC2 operational events
* GitHub for documentation and traceability
* PowerShell, SSH and RDP for validation and operations



---





\## Documentation Structure



* `architecture.md` - Jira system and process architecture
* `jira-software/`  - Delivery and Implementation tracking
* `jira-service-management/` - ITSM and operational workflows



---



\## Audience



This documentation is intended for:



* Cloud Operations Engineers
* DevOps Engineers (Operations-focused)
* Cloud Operations Analyst
* SRE
* Technical reviewers and interviewers

















* 
