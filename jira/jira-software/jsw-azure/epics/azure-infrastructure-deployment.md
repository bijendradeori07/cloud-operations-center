Md





\# Epic: Azure Infrastructure Deployment



\## Epic Objective

Design, deploy and organize core Azure Infrastructure components following best practices for scalability, security and maintainability.



\## Scope

* Networking Foundations
* Compute Resources (Linux \& Windows)
* Storage dependencies
* Diagnostics and baseline configuration



\## Linked Stories



|             Story                  |               Description                |                    Reference                      |

|------------------------------------|------------------------------------------|---------------------------------------------------|

| Design Azure Network Architecture  | VNet, Subnets, Address Space design      | stories/[azure-network-architecture.md](../stories/azure-network-architecture.md)             |                                    |                                    |                                          |                                                   |

| Create Azure Resources Groups      | Logical Separation and Governance        | stories/[azure-resource-group-standards.md](../stories/azure-resource-group-standards.md)         |

| \& Naming Standards                 |                                          |                                                   |

|                                    |                                          |                                                   |

| Deploy Windows Server VM           | Windows Workload Deployment              | stories/[deploy-windows-vm.md](../stories/deploy-windows-vm.md)                      |

|                                    |                                          |                                                   |

| Deploy Linux Server VM             | Ubuntu Linux Workload Deployment         | stories/[deploy-linux-vm.md](../stories/deploy-linux-vm.md)                        |

|                                    |                                          |                                                   |

| Configure Azure Storage Account    | Shared storage for diagnostics \& services| stories/[azure-storage-account.md](../stories/azure-storage-account.md)                  |

|                                    |                                          |                                                   |

| Enable Boot Diagnostics            | VM startup and troubleshooting support   | stories/[boot-diagnostics.md](../status/boot-diagnostics.md)                       |

|------------------------------------|------------------------------------------|---------------------------------------------------|





\## Success Criteria

* Infrastructure deployed in correct resource groups
* Networking comnfigured and validated
* VMs accessible and operatiional
* Diagnostics enabled and verified
