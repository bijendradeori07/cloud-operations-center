Md







\# Change Management



\## Purpose

Ensure standardized, controlled and auditable changes across multi-cloud infrastructure(Azure \& AWS) while minimizing risk and service disruption.



\## Change Types

* Standard Change (Low-risk, pre-approved)
* Normal Change (requires approval)
* Emergency Change (Immediate action to restore service)



\## Change Scope

* Azure Infrastructure
* AWS Infrastructure
* Networking
* Security
* Monitoring \& Backup



\## Change Workflow

1. Change request creation
2. Risk and impact assessment
3. Approval (CAB/Approver)
4. Scheduled Implementation
5. Validation and Testing
6. Change Closure with documentation



\## Risk Assessment Factors

* Service Impact
* Downtime required
* Security implication
* Multi-Cloud dependency impact



\## Multi Cloud Change Execution



\### Azure Changes

* NSG rule updates
* VM size resizing (vertical scaling)
* Backup Policy configuration or  modification
* Monitoring and alert tuning
* Log Analytics Workspace changes
* Storage account configuration updates



\### AWS Changes

* Security Group rule modification
* EC2 instance type changes
* EBS volume resize
* CloudWatch alarm configuration
* Nginx configuration updates
* Snapshot and backup configuration



All Changes are tracked, approved and documented through Jira Service Management.



\## Rollback Strategy

* Revert NSG / Security Groups rules
* Restore VM / EC2 from backup
* Rollback configuration changes
* Scale down to previous VM / instance size



\## Tools Used

* Azure Portal
* Azure Powershell
* Azure Monitor
* AWS Management Console
* AWS EC2
* AWS Security Groups
* AWS CloudWatch
* Jira Service Management
