Md







\# Jira Architecture – Cloud Operations Context



This document describes the \*\*architecture and role of Jira\*\* within the overall \*\*Cloud Operations Center\*\*. 



Jira acts as the \*\*single source of truth\*\* for both planned work and operational activities across Azure and AWS environments.



---



\## Architectural Role of Jira



Jira is positioned between:



* Cloud infrastructure (Azure and AWS)
* Monitoring and alerting systems
* Human operators and engineering teams
* Documentation and change records



It provides structure, traceability, and governance for cloud operations.



---



\## Dual-Track Jira Architecture



The Jira architecture is intentionally split into two tracks:



1\. Delivery Track (Jira Software)



Used for:

* Architecture implementation
* Infrastructure provisioning
* Configuration tasks
* Documentation updates



This track focuses on \*\*planned, project-based work\*\*.



---



2\. Operations Track (Jira Service Management)



Used for:

* Incident response
* Problem investigation
* Change control
* Service requests



This track focuses on \*\*unplanned or operational work\*\*.



---



\## Work Separation Model



|         Type of Work            |      Jira Application       |

|---------------------------------|-----------------------------|

| Planned changes                 |  Jira Software              |

| Operational incidents           |  Jira Service Management    |

| Root cause analysis             |  Jira Service Management    |

| Approved infrastructure updates |  Jira Service Management    |

| Documentation updates           |  Jira Software              |

|---------------------------------|-----------------------------|



This separation prevents operational noise from impacting delivery work.



---



\## Alert-to-Action Flow



1\. Cloud monitoring detects an event

2\. Operations team reviews the event

3\. Jira Service Management issue is created

4\. Incident or request is handled

5\. If required, a change is raised and approved

6\. Implementation work is tracked in Jira Software

7\. Documentation is updated in GitHub



---



\## Traceability Model



Jira enables traceability between:



* Alerts and incidents
* Incidents and problems
* Problems and changes
* Changes and implementation tasks
* Tasks and GitHub documentation







This supports auditability and operational clarity.



---



\## Architectural Principles



* Clear separation of delivery and operations
* ITIL-aligned service management
* Documentation-driven operations
* Minimal coupling between tools
* Human-in-the-loop decision making



---



\## Relationship to Other Architecture Layers



* \*\*Root architecture\*\* describes the full cloud system
* \*\*Jira architecture\*\* describes work and operations flow
* \*\*JSM architecture\*\* describes ITSM internals
* \*\*Jira Software architecture\*\* describes delivery structure



Each layer increases detail without duplication.















