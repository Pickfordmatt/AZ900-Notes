## Core Azure - Architectual Components

#### Regions
***
Over 60 Regions now in Azure, these are geographical areas where datacenters sit. Not all are available to all customers, such as some specified just for Government. 

- Paired Regions

  - Every region hhas another region trusted as a pair
  - The data link between each pair is the highest possible
  - Software updates only happen on one region of the pair at a time for stability
  - If multiple regions go down, one of the pair is treated a priority
  - Data in one region is mirrored in the other.

- Example Pairs
  - Canada (Canada Central - Canada East)
  - Europe (North Europe - West Europe)
  
#### Availability Zones
***
- Regions are broken down into availability zones.
- An availability zone is a physically seperate datacenters, so own power/cooling/networking. 
- The more availability zones, the less likely you will experience an outage should there be a problem with a data center. 

#### Resource Groups
*** 
- Resource groups are used to break up your Azure services by small subsets such as a project. Under a resource group you may have some virtual machines and databases, or many more depending on the needs of the project. 

#### Subscriptions
***
- A subscription is a billing unit - i.e. where to be charged.
- Different departments can use seperate subscriptions so that each department only pays for the service they use. This makes it easier to track costs. 
- Every single resource in Azure must be aligned to a subscription. 

#### Management Groups
***
- Management groups allow you to create a top down governance, so that subscriptions below a management group have the rules applied. You can also nest management groups so that rules can be applied to multiple groups more granularly. 

## Core Azure - Resources

6 Different types of resources
- Compute (Apps/VMs etc)
- Networking (Way in which apps can communicated with each other)
- Storage (How you can store data in the cloud)
- Database (Tables/Columns etc)
- Azure Marketplace (Where you find services, some not made by Microsoft)

#### Compute Services
***
Virtual Machines / App Services / Azure Container Instances / Azure Kubernetes Service / Windows Virtual Desktop

- Virtual Machine (Infrastructure-as-a-service)
  - Take an existing machine from your environment and put it in the cloud
  - Windows / Linux etc (Depends on what the cloud provider gives you the choice of)
  - A portion of a physical machine
  - Full control over the operating system as if you physically at the machine 
  - Ability to choose horsepower (CPU/RAM/Disk Size/IOPs/etc)
    
- App Services (Platform-as-a-service)
  - Package your code and Azure will execute in the cloud
  - Promise of performance but not ability to access underlying hardware

- Container Instances
  - Containers contain everything the app needs to run
  - Fastest and easiest way to deploy
  - Azure Container Instance - ACI Single instance
  - Azure Kubernetes Service - AKS runs on a cluster of servers

- Windows Virtual Desktop
  - Desktop version of Windows that runs in the cloud
  - You can access your apps from anyway with internet
  - Runs on Azure

#### Networking Services
***
Connectivity Services / Protection Services / Delivery Services / Monitoring Services

- Connectivity 
  - Virtual Network is emulating a physical network 
  - VPN connects two networks as if they were on the same networking using a gateway
  - ExpressRoute is a high-speed private connection to Azure (Requires a physical piece of hardware)

- Protection Services
  - DDoS Protectiion 
  - Azure Firewall
  - Network Security Group (ACL Based, Same as AWS Security Groups)
  - Private Link 
 
#### Storage Services
*** 

- General Purpose Storage
  - Container Storage
  - Tables
  - Queues
  - File Storage
  
  - Settings
    - Access Tiers (Hot,Cool,Archive) - Hot is default, cool is less to store but more for read and writes. Archive is the cheapest but most expensive when you read/write. 
    - Performance ties (Standard / Premium) - Pay extra for faster read/write
    - Location - Some regions are more expensive, however you may wish to pay more for less latency if closer to the file geographically
    - Redundancy - Azure by default replicates each file 3 times, can increase to globally redunant which will be 6 copies
    - Failover - Can replicate to multiple regions in case of region fallover.

- Disk Storage
  - Pay for reservation of disk
  - Costs the same regardless of how much storage you use
  - Commonly used for the underlying disk of a Virtual Machine. 
  
- Configuration Storage Account Considerations
  - Soft Delete - Files are only removed however not deleted for a period of time so that you can recover accidentally deleted files. 

#### Database Services Covered
***
Cosmos DB / Azure SQL Database / Azure Database for MySQL / Azure Database for PostgreSQL / SQL Managed Instance

 - Cosmos DB (NoSQL Storage)
  - Designed to be extremely fast
  - Supports many open-source APIs and protocols
  - Great for small bits of data that need to be fast
  - Can be replicated around the world, which would be great for games

- Azure SQL Database
  - Runs on the SQL Server Engine
  - Relations
  - Easily scaleable
  - Easy to replicate
  - Easy to migrate from on prem SQL DB. 

- Azure MySQL
  - Same as MySQL on prem

- Azure Database for Postgresql 
  - Great for large complex setups / clusters etc
  - Easy to migrate into the cloud
  - Open source

- SQL Managed Instance
  - Most compatible with existing SQL Server
  - Fully managed by Azure
  - Always up to date
