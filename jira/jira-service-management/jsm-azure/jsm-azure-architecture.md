Md





\# Jira Service Management - ITSM Architecture



This documents describes the \*\*IT Service Management (ITSM)\*\* implementation using \*\*Jira Service Management (JSM)\*\* for cloud operations.



The architecture follows \*\*ITIL-aligned practices\*\* to manage operational events originating from Azure environments.



---



\## Architectural Overview



The ITSM architecture is designed to handle the full operational lifecycle:



* Detection of issues via cloud monitoring
* Incidents creation and triage 
* Root Cause Analysis through problem management
* Controlled infrastructure changes 
* SLA-driven response and resolution tracking 



---



\## Event-to-Incident flow



1\. Cloud monitoring detects an event

* VM down
* High CPU utilization
* Network or access failure



2\. Event is reviewed by operations

3\. Incidents is created in Jira Service Management

4\. Incidents is categorized, prioritized and assigned

5\. Resolution steps are executed and validated 

6\. Incidents is closed with documentation



---



\## Incidents Management Design



Incidents are classified based on:

* Impact (single VM vs multiple services)
* Urgency (production vs non-production
* Type (availability, performance security)



Each incidents includes:



* Description of issue
* Affected resource
* Initial diagnosis
* Resolution steps
* Post-resolution notes



---



\## Problem Management Design



Problems are created when:



* Incidents recur
* Root cause is not immediately clear
* Long-term corrective action is required



Problem records include:



* Linked incidents
* Root Cause Analysis(RCA)
* Preventive actions
* Reference to relate changes



---



\## Change Management Design



Changes are used for:



* NSG rule updates
* OS or package updates
* Configuration changes
* Security hardening


Each changes include:



* Change description
* Risk and impact assessment
* Approval status
* Implementation and rollback plan



---



\## Service Request Design



Service Requests Cover:



* SSH or RDP access requests
* Monitoring access
* Backup and recovery request
* Operational support tasks



Requests follow a standardized approval and fulfillment workflow.



---



\## SLA Architecture



SLAs are defined based on:

* Incident priority
* Business impact
* Response and resolution targets



SLA tracking ensures:

* Timely response to incidents 
* Visibility into operational performance
* Continuous service improvement



---



\## Architectural Principles



* Clear separation between incidents, problems and changes
* Traceability between operational events and actions
* Alignment with cloud monitoring and operations 
* Documentation-first approach for audits and reviews



---



\## Visual Architecture



Refer to `itsm-flow.png` for a visual representative of the ITSM workflow

from the cloud events to resolution and closure.











