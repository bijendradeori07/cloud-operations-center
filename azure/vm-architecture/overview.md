Md





\# Azure VM Architecture - Windows \& Linux



\## Overview

This project demonstrates deployment and management of Windows \& Linux virtual machines in Azure following enterprise best practices.



\## Key Highlights

* Windows Server VM accessed via RDP
* Ubuntu Linux VM accessed via SSH
* Separate resource group for individual workloads
* Shared resource group for common platform services
* Custom virtual network and subnet design
* Network Security Group(NSG) applied at subnet level
* Centralized monitoring using Log Analytics
* Alerts configured for VM availability and performance
* Backup enabled using Recovery Services Vault(RSV)
* VM administration performed using PowerShell



\## Architecture Design

\### Workload Resources Groups:

* Windows VM Resource Group
* Linux VM Resource Group



!\[Resource Group Overview](screenshots/resource-groups-overview.png)



\### Shared Resource Group:

* Log Analytics Workspace
* Recovery Vault Service
