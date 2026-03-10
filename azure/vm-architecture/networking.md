## Networking - Vnet, Subnet and NSG

## Virtual Network
* Custom Vnet created
* Address space planned manually

## Subnets
* Separate subnets for Windows and Linux VMs
* Improved Isolation and control

## Network Security Groups
* NSG associated at subnet level
* Inbound rules:
   - SSH(22): Restricted to my IP
   - RDP(3389): Restricted to my IP
   - HTTP(80) : Public access for testing
   - Default deny for all other inbound traffic

This ensures secure administrative access following least-privilege principles.

![NSG Inbound Rules](screenshots/nsg-inbound-rules.png)


## Reasoning
Applying NSG at subnet level simplifies management and follows Azure best practices.

