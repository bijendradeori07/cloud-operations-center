Md





\# Incident Management



\## Purpose

Restore normal service operation as quickly as possible and minimize business impact



\## Incident Types

* VM / Instance Down
* High CPU Utilization
* Disk Space Full
* Network Connectivity Issue
* SSH / RDP Access Failure
* Web Service Unavailability (Nginx)



\## Incident sources

* Azure Monitor Alerts
* Azure Log Analytics
* AWS CloudWatch Alarms
* AWS EC2 Status Checks
* User-reported issues
* Automated health checks



\## Incident Workflows

1. Incident created automatically or manually
2. Initial triage and priority assignment
3. Investigation and diagnosis
4. Resolution and service restoration
5. Incident closure and documentation



\## Severity Levels

* P1: Critical (Production VM Down / EC2 Down)
* P2: High (Severe Performance degradation)
* P3: Medium (Partial service impact)
* P4: Low (Minor Issue or Warning)



\## Tools Used

* Azure Monitor
* Azure Log Analytics Workspace
* AWS CloudWatch
* AWS EC2 Health Dashboard
* Jira Service Management
* PowerShell / AWS CLI







