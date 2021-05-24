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

#### Best practises for reducing Azure costs
****
- Azure Advisor Cost Tab will make suggestions as to how you can reduce your costs
- Auto shutdown any resources when not in use (time or activity)
- Utilise cool/archive storage where possible
- Reserved instances will be at a reduced rate, however you're paying regardless if its off or on. 
- Configure billing alerts when billing exceed an expected level
- Implement policy to restrict certain expensive resources
- Autoscaling resources both up and down to run the same workloads on the required hardware
- Ensure every resource has an owner in tags


Spot pricing
- Ability to use a virtual machine when nobody is using it for a discounted price at much lower costs

#### Pricing Calculator
****
- It's impossible to calculate an exact estimate amount 
- Configurable options (Region/Tier/Subscription Type/Support Opetions/Dev-Test pricing
- You can save and export the Azure estimate for collaberotive input
- Total Cost of Ownership (

## Service Level Agreement (SLA)
***
- 2 or more Virtual Machines across 2 or more availability zones within the same Region, Microsoft promises a 99.99% uptime.
- 2 or more Virtual Machines deployed within the same availability set or in the same dedicated host group, guarented connectivity to at least one of them 99.95% of the time. 
- Any single Virtual Machine using Premium SSD or Ultra Disk, guarenteed connectivity 99.9% of the time
- Any single virtual machine with Standard SSD, guarenteed connectivity 99.5% of the time
- Any Sinle virtual machine using Standard HDD, guarenteed connectivity 95% of the time
- Load balanced endpoint using Azure Standard Load Balancer serving 2 or more health virtual machines will be available 99.99% of the time
- Basic load balancer is not included in the SLA for refunds

- Previews are not included within the SLAs
- Public preview available to everyone
- Private preview requires registration
- GA - Generally Available
