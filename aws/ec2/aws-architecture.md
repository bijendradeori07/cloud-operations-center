Md







\# AWS Architecture – Cloud Operations Center



\## Architecture Purpose



This document defines the \*\*AWS infrastructure architecture\*\*

used within the \*\*Cloud Operations Center (Multi-Cloud)\*\* project.



The AWS architecture demonstrates how \*\*AWS workloads are securely deployed

and operated\*\*, and how they fit into a broader multi-cloud operations model.



---



\## Architectural Scope



The AWS architecture includes:



* EC2-based compute
* Network security using Security Groups
* SSH-based access control
* Application hosting using Nginx
* Instance-level storage using EBS



\*\*Not implemented in the current phase:\*\*



* Managed AWS services (RDS, ALB, ECS)
* Advanced automation and CI/CD pipelines
* Infrastructure as Code (Terraform / CloudFormation)
* Kubernetes-based container orchestration





These capabilities are intentionally excluded from the current phase

to keep the focus on \*\*Cloud Operations and ITSM workflows\*\*.

They are planned for future iterations of the Cloud Operations Center.



---



\## High-Level AWS Architecture





+--------------------------------------+

|                AWS                   |

|                                      |

|   +------------------------------+   |

|   |        EC2 Instance          |   |

|   |    - Linux OS                |   |

|   |    - Nginx Web Server        |   |

|   |    - SSH Access              |   |

|   +-----------+------------------+   |

|               |                      |

|   +-----------v------------------+   |

|   |        EBS Volume            |   |

|   |    - OS Disk                 |   |

|   |    - Application Data        |   |

|   +------------------------------+   |

|                                      |

|   +------------------------------+   |

|   |       Security Group         |   |

|   |    - SSH (Restricted)        |   |

|   |    - HTTP (Public)           |   |

|   +------------------------------+   |

|                                      |

|   +------------------------------+   |

|   |        CloudWatch            |   |

|   |    - Instance Health         |   |

|   |    - Basic Metrics           |   |

|   +------------------------------+   |

|                                      |

+--------------------------------------+







---



\## Compute Layer



* Amazon EC2 instance running Linux
* Instance sized for cost-efficient operations
* Used to host and validate Nginx web server
* Operated via SSH using key-based authentication



---



\## Networking \& Security



* EC2 instance deployed within AWS VPC
* Network access controlled using Security Groups
* Inbound rules include:

&nbsp; - SSH (22) restricted to specific source

&nbsp; - HTTP (80) allowed for public access

* Outbound traffic allowed as per default rules



This design follows \*\*least-privilege network security principles\*\*.



---



\## Storage Layer



* Amazon EBS volumes attached to EC2
* Used for:

&nbsp; - Operating system storage

&nbsp; - Application and configuration data

* Storage lifecycle tied to EC2 instance



---



\## Monitoring \& Operations



* Basic EC2 monitoring via AWS CloudWatch
* Instance health and status visibility
* Operational validation performed via SSH



Monitoring depth is intentionally limited

to keep focus on \*\*Azure-led centralized operations\*\*.



---



\## Integration with Cloud Operations Center



AWS integrates with the Cloud Operations Center by:



* Providing parallel cloud infrastructure to Azure
* Being governed through Jira delivery tracking
* Participating in ITSM workflows for incidents and changes
* Maintaining documentation and evidence in GitHub



---



\## Design Principles Applied



* Simplicity and clarity
* Secure access by default
* Least-privilege networking
* Operational transparency
* Clear separation from Azure infrastructure



---



\## Summary



The AWS architecture demonstrates a \*\*clean, secure, and operable EC2-based workload\*\*

that complements the Azure enterprise environment.



Together, AWS and Azure form a \*\*realistic multi-cloud Cloud Operations Center\*\*

focused on operations, governance, and support.



















