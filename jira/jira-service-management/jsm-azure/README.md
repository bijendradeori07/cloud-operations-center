Md





\# Jira Service Management -Cloud operations



This section documents the \*\*IT Service Management (ITSM)\*\* implementation using \*\*Jira Service Management (JSM)\*\* for cloud operations.



It focuses on how operational events from \*\*Azure\*\* are handled using structured ITSM practiced such as \*\*Incident, Problem, Change and Service Request Management\*\*.



---



\## Scope



The Jira Service Management setup covers:



* Incident management for production issues (VM down, high CPU, access failure)
* Problem management for recurring or root-cause issues
* Change management for infrastructure and security updates
* Service request for access and operational needs
* SLA request for access and operational workflow documentation



This section complements the \*\*delivery tracking\*\* done in Jira Software.



---



\## ITSM Modules Documented



|     Module       |                    Description                        |  

|------------------|-------------------------------------------------------|     

| Incidents        | Handling Outages and alerts from cloud monitoring     |

| Problems         | Root Cause analysis for recurring issues              |

| Changes          | Controlled changes to cloud infrastructure            |

| Service Requests | Access, Configuration and Support requests            |

| SLA              | Service-Level objectives and response times           |

|------------------|-------------------------------------------------------|





---



\## Integration Context



Jira Service Management is integrated conceptually with the following operational components:



* Azure VM and Infrastructure events
* Azure Monitor and Log Analytics alerts
* Operational validation via PowerShell and SSH/RDP
* GitHub documentation and change traceability



--- 



\## This documentation is intended for :



* Cloud Operations Engineer
* Cloud Operations Analyst
* DevOps Engineer (Operation-focused)
* SRE
* Technical Reviewers and Interviewers













