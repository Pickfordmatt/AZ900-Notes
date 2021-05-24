## Azure Security

#### Key Vault
***
Central secure repo for your secrets, certificates and keys 

- This may be secrets for a web app so that they do not need to be stored within configuration files, also it limits who has access to these secrets.

- The ability to generate and store encryption keys

#### Sentinal
***
- Centralises all log files from various resources
- Analyses the collected logs to detect threats
- Can write custom detections
- Ability to investigate incidents
- Build custom runbooks to fix any issues

#### Dedicated Hosts
***
Azure allows users to reserve whole servers so that no software vulns can potentially expose multiple tennated devices. 

#### Defence in Depth
***
- Data - i.e. virtual network endpoint
- Application - i.e. API Management
- Compute - i.e. Limit Remote Dekstop access, Windows Update
- Network - i.e. NSG, use of subnets, deny by default
- Perimeter -i.e. DDoS, Firewalls
- Identity & Access - i.e. Azure AD
- Physical - i.e. Door locks and key cards

#### Network Security Groups
***
- These work in the same way for a subnet as they do in AWS Security Groups
- Access Control List based rules

#### Azure Firewall
- The Azure Firewall will inspect data and try to find trends and identify threats
- Basic firewall will try and prevent L3/L4 DDoS Attacks
- WAF with the basic firewall
- Logging and Alerting is only available to the Standard package

## Managing Azure Costs
#### Overview of Azure Pricing
***
Pay per usage (Consumption Model)
  - Functions
  - Logic Apps
  - Storage
  - Outbound Bandwidth
  - Cognitive API

Pay for time (per second)
  - Billing starts the second a virtual machine starts, and stops the second it stops
    - You will still be paying for any used storage
  - Discounts for 1 year or 3 year commitments (Reserved Instance)

Per per bandwidth
  - First 5Gb outbound free
  - All inbound traffic is free
