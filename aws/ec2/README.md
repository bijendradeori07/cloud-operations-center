Md





\# AWS Infrastructure – Cloud Operations Center



This directory documents the \*\*AWS infrastructure\*\*

implemented as part of the \*\*Cloud Operations Center (Multi-Cloud)\*\* project.



The AWS setup focuses on \*\*compute, security, access control, and basic operations\*\*

to demonstrate how AWS workloads are operated alongside Azure

in a multi-cloud environment.



---



\## Scope



The AWS implementation covers:



* EC2-based compute
* Secure access using SSH key-based authentication
* Network security using Security Groups
* Linux-based workload hosting
* Basic operational validation



This section complements the \*\*Azure enterprise architecture\*\*

by providing AWS-side infrastructure and operations visibility.



---



\## Components Implemented





|  Component  |         Description          |

|-------------|------------------------------|

| Compute     | Amazon EC2 (Linux)           |

| Networking  | VPC-level networking         |

| Security    | Security Groups              |

| Access      | SSH key-based authentication |

| Application | Nginx web server             |

| Storage     | EBS volumes attached to EC2  |

|-------------|------------------------------|







---



\## Documentation Structure





|        File           |                Description                  |

|-----------------------|---------------------------------------------|

| `aws-architecture.md` | AWS infrastructure architecture             |

| `steps.md`            | EC2 provisioning and configuration steps    |

| `security-groups.md`  | Security Group rules and access design      |

| `screenshots/`        | Redacted evidence of AWS configuration      |

|-----------------------|---------------------------------------------|







---



\## Operational Context



AWS infrastructure is operated using:



* AWS Management Console
* SSH access for Linux administration
* GitHub for documentation and evidence
* Jira for delivery tracking and operational governance



---



\## Relationship to Other Sections



* Azure provides enterprise-scale operations and monitoring
* AWS provides parallel cloud infrastructure operations
* Jira governs delivery and ITSM workflows across both clouds











