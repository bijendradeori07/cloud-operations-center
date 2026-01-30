Md





\# Service Request Management



\## Purpose

Handle standard, repeatable service requests efficiently across Azure and AWS environments with minimal operational overhead



\## Common Service Request



\### Compute \& Access

* Azure VM access request (SSH / RDP)
* AWS EC2 access request (SSH / key pair)
* Bastion /Jump host access
* Temporary admin access (RBAC/ IAM)



\### Infrastructure Provisioning

* New Azure Virtual Machine
* New AWS EC2 instance provisioning
* VM size / instance type change
* Attach or detach disks



\### Storage

* Azure Storage Account Access
* Blob / File Share access
* EBS volume attach / resize
* Backup restore request (Azure Recovery Services / AWS snapshots)



\### Networking \& Security

* NSG rule change (Azure)
* Security Group rule change (AWS)
* VNet / Subnet access request
* Public IP assignment or removal



\### Monitoring \& Visibility

* Enable Azure Monitor for VM
* Enable AWS CloudWatch alarms
* Log Analytics workspace access
* Monitoring dashboard access







\## Request Workflow

1. User submits service request
2. Request categorization and validation
3. Approval (if required)
4. Fulfillment by operations team
5. User confirmation
6. Request Closure



\## Approval Scenarios

* Production access requests
* Firewall / Security rule changes
* VM provisioning in production
* Backup restore operations



\## Fulfillment Teams

* Cloud Operations
* Security Team
* Infrastructure Team



\## Automation Opportunities

* VM provisioning via templates
* Access assignment using RBAC/IAM
* Monitoring and alert enablement
* Standard storage and backup configuration



\## Tools Used

* Jira Service Management
* Azure Portal
* AWS Management Console
* PowerShell
* Azure CLI
* AWS CLI









