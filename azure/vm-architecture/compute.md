MD



\# Compute - Virtual Machines

 

\## Windows Virtual Machines

* OS: Windows Server
* Access: RDP(3389)
* Used for GUI-Based administration and testing
* Managed using Azure Portal and Powershell
* Deployed in a dedicated workload resource group



!\[Windows VM Overview](screenshots/vm-windows-overview.png)



\## Linux Virtual Machines

* OS: Ubuntu LTS
* Access: SSH (22)
* Used for Linux-based workload operations
* Managed using Powershell and SSH





!\[Linux-VM-Overview](screenshots/vm-linux-overview.png)



\## SSH Access Configuration

* Key-based Authentication used for Linux VM
* Password Authentication disabled for SSH
* SSH and RDP restricted to admin public IP via NSG
* PEM key for Authentication



!\[SSH Login Using Key](screenshots/ssh-login-ubuntu-using-key.png)



\##VM Configuration

* Availability: Single-Instance (lab setup)
* Size selected based on cost efficiency



\## Web Server

* Nginx installed on Ubuntu VM
* Used to validate HTTP access and NSG rules
* Confirms NSG rules and network flow
* Integrated with Azure monitoring and alerts





