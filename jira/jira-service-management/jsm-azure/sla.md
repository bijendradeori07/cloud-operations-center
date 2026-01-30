Md





\# Service Level Agreement (SLA)



\## Scope

This applies to all Jira Service Management activities related to multi-cloud nfrastructure hosted on Azure and AWS.



\###Covered areas:

* Incident Management
* Change Management
* Service request Management 
* Problem Management





\## SLA Objectives

* Minimize service disruption
* Ensure predictable response and delivery timelines
* Maintain operational reliability across Azure and AWS environments
* Enforce accountability and auditability



---





\## Incident Management SLA



\### Incident SLA Metrics

* Time to First response
* Time to Resolution



\### Incidents SLA Metrics



|    Priority   |                   Impact Description                   |     Response Time      |     Resolution Time         | 

|---------------|--------------------------------------------------------|------------------------|-----------------------------|

|      P1       |         Critical (VM / EC2 down, Production)           |        15m             |            4h               |

|      P2       |         High ( Severe Performance degradation )        |        30m             |            8h               |

|      P3       |         Medium ( Partial service impact )              |         4h             |           24h               |

|      P4       |         Low ( Minor issue / Warning )                  |        24h             |           72h               |

|---------------|--------------------------------------------------------|------------------------|-----------------------------|



\### Incidents Escalation

* P1 \& P2 Incidents auto-escalated
* CloudOps team notified immediately
* Root Cause Analysis (RCA) mandatory for P1 \& P2



---



\## Change Management SLA



\### Change SLA Metrics

* Time to Approval
* Implementation Window
* Post-change Validation Time



\### Change SLA Metrics



|  Change Type  |      Approval Time          |   Implementation Window   |   Rollback Plan   |       

|---------------|-----------------------------|---------------------------|-------------------|

|   Standard    |      Pre-Approved           |        Scheduled          |     Optional      |

|    Normal     |      Within 24h             |   Approved Change Window  |    Mandatory      |

|   Emergency   |      Within 1h              |        Immediate          |    Mandatory      |

|---------------|-----------------------------|---------------------------|-------------------|



\### Change Validation SLA

* Post-change validation completed within 2 hours
* Monitoring via Azure Monitor and AWS CloudWatch
* Rollback initiated on failure or alert reach



\### Change Escalation

* Failed change triggers Incident
* Post Implementation Review (PIR) required



---



\## Service Request SLA



\### Service Request SLA Metrics

* Fulfillment time



|       Request Type        |  Fulfillment Time  |

|---------------------------|--------------------|

|  VM / EC2 Access request  |      24h           |

|    NEW VM Provisioning    |      48h           |

|   Backup Restore Request  |      4h            |

| Monitoring Access Request |      24h           |

|---------------------------|--------------------|



\### SLA Monitoring and Reporting



\### Tools used

* Jira Service Management SLA engine
* Azure Monitor
* Azure Log Analytics
* AWS CloudWatch



\### SLA Breach Handling

* Automatic Breach notification
* Escalation to CloudOps team
* Review and corrective action



---





\## Review \& Improvement

* SLA reviewed periodically
* Adjustment made based on incidents trends and business needs



---





\## Problem Management SLA 



\### Problem SLA Metrics

* Time to Problem review
* Time to Root Cause Analysis (RCA)
* Time to Permanent Resolution



\### Problem SLA Metrics



|   Priority   |          Problem Type           |   Review Time   |   RCA Completion   | Resolution Target |

|--------------|---------------------------------|-----------------|--------------------|-------------------|

|     P1       |  Critical Recurring Incident    | 1 business day  |  3 business days   |  5 Business days  |

|     P2       |  High-impact recurring issue    | 2 business days |  5 business days   |  10 business days |

|     P3       |  Medium-impact issue            | 3 business days |  7 business days   |  15 business days |

|     P4       |  Low-impact / Informational     | 5 business days |    As required     |    As required    |

|--------------|---------------------------------|-----------------|--------------------|-------------------|





\### Problem Workflow SLA 

* Problem created from one or more incidents 
* RCA initiated within SLA timeline
* Permanent fix proposed as change request
* Problem closed after fix validation



\### Tools Used

* Jira service Management
* Azure Monitor \& Log Analytics
* AWS CloudWatch
* Activity Logs



\### Governance 

* RCA documentation mandatory for P1 \& P2 problems
* Problems reviewed during periodic operations review

































