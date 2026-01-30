Md





\# Jira Workflow - Cloud Operations Center



\## Purpose

This documents describe how work flows through Jira for cloud delivery and cloud operations in this project.



---



\## Delivery Workflow (Jira Software)



\*\*Epic → Story → Task → Subtasks\*\*



Flow:

1. Epic created for major cloud initiative (e.g Azure VM Architecture)
2. Stories created for individual components (VM, VNet, NSG, Monitoring)
3. Tasks created for implementation work
4. Sub-tasks created for validation, testing and documentation



\*\*Status Flow\*\*

* To Do
* In Progress
* In Review
* Done



---



\## Operation Workflow (Jira Service Management)



\*\*Alert/Request → Incident → Problem/Change → Closure\*\*



\### Incident Flow

1. Alert triggered (VM Down, CPU High, etc)
2. Incident created in JSM
3. Initial investigation performed
4. Incident resolved or escalated to problem



\### Problem Flow

1. Recurring incidents identified
2. Root Cause Analysis performed
3. Permanent fix identified
4. Problem closed



\### Change Flow

1. Change Request created (e.g NSG rule update)
2. Impact analysis and rollback plan added
3. Change implemented
4. Validation completed
5. Change closed



---



\## Integration Points



* Monitoring alerts lead to Incidents creation
* Jira issues are referenced in GitHub commits
* Documentation updates tracked as tasks or sub-tasks



---



\## Outcome 



This workflow ensures structured delivery, controlled changes and traceable cloud operations.















