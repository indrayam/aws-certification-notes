# AWS Certified Cloud Practitioner (CCP) 2020

## AWS CCP Home
[AWS CCP 2020](https://aws.amazon.com/certification/certified-cloud-practitioner/)

## Preparation Materials
- [acloud.guru: Introduction to Cloud Computing](https://learn.acloud.guru/course/aws-technical-essentials/dashboard) ✅
- [acloud.guru: Introduction to AWS](https://learn.acloud.guru/course/aws-technical-essentials/dashboard) ✅
- [Richard Jones: AWS Certified Cloud Practitioner, 1/e **May 2019**](https://learning.oreilly.com/learning-paths/learning-path-aws/9780135940037/?autoplay=false) 🚧
- [acloud.guru: AWS Certified Cloud Practitioner 2020](https://learn.acloud.guru/course/aws-certified-cloud-practitioner/dashboard)
- [Michael Shannon: AWS Certified Cloud Practitioner Exam Crash Course **May 2019**](https://learning.oreilly.com/live-training/courses/aws-certified-cloud-practitioner-exam-crash-course/0636920260257/)
- [freeCodeCamp: AWS Certified Cloud Practitioner Training 2020 - Full Course **Oct 2019**](https://www.youtube.com/watch?v=3hLmDS179YE)

## Exam Format
- 90 mins
- ~65 questions
- Your results for the examination are reported as a score from 100–1,000, with a minimum passing score of 700. Your score shows how you performed on the examination as a whole and whether or not you passed. 

## Exam Domains Categories
**Domain 1: Cloud Concepts**
- Define the AWS Cloud and its value proposition
- Identify aspects of AWS Cloud economics
- List the different cloud architecture design principles

**Domain 2: Security and Compliance**
- Define the AWS shared responsibility model
- Define AWS Cloud security and compliance concepts
- Identify AWS access management capabilities
- Identify resources for security support

**Domain 3: Technology**
- Define methods of deploying and operating in the AWS Cloud
- Define the AWS global infrastructure
- Identify the core AWS services
- Identify resources for technology support

**Domain 4: Billing and Pricing**
- Compare and contrast the various pricing models for AWS
- Recognize the various account structures in relation to - billing and pricing
- Identify resources available for billing support

### Exam-centric AWS Services
- AWS Global Infrastructure
  + 24 Regions (3 more coming)
  + 77 Availability Zones
  + 217 PoP (205 Edge; 12 Regional Caches)
- Networking & Content Delivery
  + VPC (Virtual Private Cloud)
  + Route53
  + CloudFront
  + DirectConnect
- Compute
  + EC2 (Elastic Compute Cloud)
    - EBS (Elastic Block Store): Virtual disk that you attach to your EC2.
  + ECS (EC2 Container Service) *Not an Exam Topic*
  + Elastic Beanstalk 
  + Lambda *Not an Exam Topic*
  + Lightsail *Not an Exam Topic*
- Storage
  + S3 (Simple Storage Service): Object storage.
  + Glacier
  + EFS (Elastic File Service): File storage. Shared. Think NFS!
  + Storage Gateway
- Databases
  + RDS (MySQL, Postgres, MariaDB, Oracle, MS SQLServer, Aurora): Relational Database
  + DynamoDB: NoSQL database.
  + Redshift: Data Warehouse solution
  + Elasticache: K/V store. Caching solution. Think Redis!
- Messaging
  + SNS (Simple Notification Service): Via email or text message or to HTTP(S) end points
  + SQS (Simple Query Service): Decouple your application by introduce async processing
  + SES (Simple Email Service): Sending and receiving emails
- Security & Identity
  + IAM (Identity and Access Management) *Comes up in all exams*
  + Inspector: Agent you install on each VM that inspects security posture of the VM
  + Certificate Manager: Think Lets Encrypt.
  + Directory Service
  + WAF (Web Application Firewall): App level firewall protection (Cross-site scripting, SQL injection etc.)
  + Artifacts: Compliance Reports/Documents
- Management Tools
  + Cloud Formation: Turn your infrastructure provisioning effort from imperative scripts to declarative scripts. Infra as Code.
  + CloudWatch: Monitor performance of things like EC2 (Disk Utilization, RAM Utilization etc.)
  + Cloud Trail: Auditing changes to your AWS environment
  + Opsworks: Chef based Config Management
  + Config: Audit + setup alerts
  + Service Catalog: For larger enterprises. Build out what they authorize to be used
  + Trusted Advisor: Give tips on your setup. Example: Cost optimization
- Desktop & App Streaming
  + Workspaces: Think VDI
  + AppStream 2.0: Streaming desktop apps to your users

## Notes
- Cloud Computing
  + On demand, self-service
  + elastic
  + metered pricing
- Service Models
  + IaaS
  + PaaS
  + SaaS
- Deployment Models
  + Private
  + Public
  + Hybrid
- What do we want from our Infra/App?
  + High Availability/Resiliency
  + Security
  + Durability
  + Performance
  + Cost-effectiveness
  + Scalability
  + Automation
- What do we want from our Process and/or Workflow?
  + Agile
  + Flexible
  + Efficient
  + Secure
- From a Business Perspective
  + Fast time to market
  + Secure, reliable data center
  + Opex over CapEx
  + No long-term commitments
  + Immediate scalability
  + Easier Cost Allocation
- AWS Cloud Value Proposition
  + On-demand resources (..get what you need, when you need it)
  + Pay as you go (..use what you need)
  + No long term commitments (..feel free to throw things away if you don't need it)
  + Highly automated (repeatable infrastructures)
  + Managed Services (with inherent high-availability, security, durability)
- AWS Global Infra
  + Regions ~27, Availability Zones ~86, Local Zones ~2, WaveLength Zones ~5, Edge Locations ~205, Regional Edge Caches ~12, Outposts
  + Regions: 
    - US West: Oregon, N. California, GovCloud (US-West)
    - US East: Ohio, N. Virgina, GovCloud (US-East)
    - Canada (Central)
    - South America: Sao Paulo
    - Europe: Spain (NEW), Ireland, London, Paris, Milan, Frankfurt, Stockholm
    - Middle East: Bahrain
    - Africa: Cape Town
    - Asia Pacific: Mumbai, Hong Kong, Seoul, Tokyo, Japan (New), Singapore, Indonesia (New), Sydney
    - Mainland China: Beijing, Ningxia
  + Choosing a Region
    - Available Services and Features
    - Cost of Services
    - Latency, Proximity to Users
    - Disaster Recovery
    - Security & Compliance
  + Availability Zones:
    - Each AZ is at least one, sometimes 2 or more, DCs very close to each other
    - AZs are connected with private fiber
  + Edge Locations
    - These locations power AWS CDN (CloudFront) and DNS (Route53) services
- Networking using VPC
  + Logically isolated network. It cannot connect to other VPC or outside world without configuration
  + Created per account, per Region
  + Embrace the idea of multiple VPCs for your App Architecture
  + One VPC spans one single Region. Translation: One VPC can use "all" AZs within one Region
  + VPCs can peer with one another. However, in order for that to happen, the CIDR block for the two VPCs trying to peer should not have overlapping IP addresses
  + VPCs allow us to create Internet and VPN Gateways
  + VPCs provide numerous security mechanisms: Security Groups etc.
  + There is a soft limit of 5 VPCs per Region, per Account. However, you can request to have that be increased
- Subnets in VPC
  + Divide VPCs into Subnets
  + Subnets are tied 1:1 with AZs
  + For example, if the VPC CIDR is set to 10.2.0.0/16, by definition it has a total of ~65k addresses it can work (read, subnet) with. If we the region has 3 AZs and we decided to create 3 subnets, one for each AZ, we could create the following subnets:
    - 10.2.0.0/24 can have a maximum of 2^8 - 2 = 254 Hosts in the Subnet
      Network IP: 10.2.0.0/24
      Broadcast IP: 10.2.0.255/24
      Usable IP Addresses: 10.2.0.1 to 10.2.0.254
    - 10.2.1.0/24 can have a maximum of 2^8 - 2 = 254 Hosts in the Subnet
      Network IP: 10.2.1.0/24
      Broadcast IP: 10.2.1.255/24
      Usable IP Addresses: 10.2.1.1 to 10.2.1.254
    - 10.2.2.0/28 can have a maximum of 2^4 - 2 = 14 Hosts in the Subnet
      Network IP: 10.2.2.0/28
      Broadcast IP: 10.2.2.15/28
      Usable IP Addresses: 10.2.2.1 to 10.2.2.14
  + Let's take a Three-Tier Architecture which includes:
    - Public LB Tier
    - Private App Tier
    - Private DB Tier
  + Each tier should have Internet Access, High Availability, Fault Tolerance along with Isolation & Security
  + In such a case, you will end up with potentially 9 unique subnets, 3 for each tier and each tier replicated across 3 AZs
  + For example, if the VPC CIDR is set to 10.2.0.0/16, we could create 9 Subnets, using the following 16 subnets by using /21:
    - 10.2.0.0/21 can have a maximum of 2^11 - 2 = 2046 Hosts in the Subnet
      Network IP: 10.2.0.0
      Broadcast IP: 10.2.7.255
      Usable IP Addresses: 10.2.0.1 to 10.2.7.254
    - 10.2.8.0/21 can have a maximum of 2^11 - 2 = 2044 Hosts in the Subnet
      Network IP: 10.2.8.0
      Broadcast IP: 10.2.15.255
      Usable IP Addresses: 10.2.8.1 to 10.2.15.254    
    - 10.2.16.0/21 can have a maximum of 2^11 - 2 = 2044 Hosts in the Subnet
      Network IP: 10.2.16.0
      Broadcast IP: 10.2.23.255
      Usable IP Addresses: 10.2.16.1 to 10.2.23.254
    - 10.2.24.0/21 can have a maximum of 2^11 - 2 = 2044 Hosts in the Subnet
      Network IP: 10.2.24.0
      Broadcast IP: 10.2.31.255
      Usable IP Addresses: 10.2.24.1 to 10.2.31.254
    - ...plus 12 more subnets like this
  + Subnets enable
    - Security via Isolation
    - Because subnets allow us to use multiple AZ, it enables High-Availability
    - Fault Tolerance
    - Performance: In order to achieve the lowest latency and best packet per sec performance, all of the machines would need to be in the same subnet in the same AZ. So, sometimes, you may have to compromise on HA for sake of Performance or vice versa
+ Routing & Firewalls
  - In any given VPC, the way traffic flows from it to anywhere else is by way of Routing. In other words, routing is the first line of defense. A firewall of sorts. Why? Because without a route, packets are just not going to flow anywhere. We can whitelist IPs to define where traffic is allowed to flow.
  - If you want hosts in a subnet inside a VPC to talk to the internet, first you create and attach an Internet Gateway (igw-1) to the VPC
  - Then create a Route Table with a definition like the following:
    10.2.0.0/16 => local
    0.0.0.0/0   => igw-1
  - Once you have created a Route Table, you attach the Route Table to the Subnet. By doing this, you enable bi-directional communication to and from the Internet. By doing this, you have technically made the Subnet a "public" subnet. Basically, a subnet is "public" if it has to and from Internet access
  - Network Access Control Lists are firewalls of the subnet as a whole. 
  - Security Groups are firewalls at the individual machine level inside a subnet. Once you define Security Groups and add machines to it, "allow" rules can be created referencing the Security Groups, not the individual VMs per se
  - By default, security groups have an implicit "Deny All" rule. All your rules are really for allowing traffic on ports "explicitly"
- Route53
  + Amazon Route 53 is Amazon's globally distributed DNS service and leverages those 200 odd edge locations. 
  + We can register domains since it is also a Registrar
  + We can use AWS as stable, reliable and fast nameservers, thanks to the edge locations again
  + It supports Public and Private DNS zones
  + Automated via API
  + Supports Health Checks
  + Routing Methods
    - Latency based Routing
    - Geographic Routing
    - Failover Routing, when used in conjunction with Health Checks
    - Weighted Sets
- AWS Hardware VPN
  - Hardware enabled IPSEC encrypted VPN tunnel
  - On the Amazon side, that tunnel is powered by two physically distinct routers in two distinct facilities
  - On the customer side, it should me made HA too by running 2 routers on their side
  - VPN connectivity is really great for admin work, for low bandwidth type of transfer
- Amazon Direct Connect
  - If there is more data to be pumped between AWS VPCs and Customer premise, Amazon Direct Connect might be better
  - Customer works with a AWS Direct Connect Provider and can setup a 1 or 10 GBPS fiber connection to the Provider
  - DX Providers already have connections to AWS
  - This is definitely prefered if you need lots of bandwidth to flow between your premise and AWS
- EC2 (Elastic Cloud Compute)
  - VMs
  - Linux or Windows
  - Xen or Nitro hypervisor
  - Bare Metal is available
  - Fixed Prices based on CPU, IO, Disk and Memory
  - Default limit is 20 per account
  - Different Billing Models
    + On-demand
    + Spot Instances
    + Reserved Instances
  - Hourly fees includes license cost of operating system
  - Rack, Chassis => Intel Xeon (CPU)/Motherboard => Hypervisor (Xen or Nitro) => EC2 Instances (VM)
  - There may be that more than one tenant on a single host
  - However, a single customer could get dedicated host
  - AMI - Amazon Machine Images
- EC2 Best Practices
  - Treat them as disposable
  - "Immutable Infrastructure"
  - Logs as Streams
  - Leverage Roles that allows us to control access to other AWS services
  - Automate Deployments
  - Monitor with CloudWatch
  - Enable scaling and self-healing with Auto Scaling
- EBS (Elastic Block Store)
  - Increase data durability of an EC2 instance
  - Used when we need higher degree of Random IO
  - Used when we need a mounted filesystem
  - Efficient protocol
  - Can be attached or detached to an EC2 in the same AZ
  - You can create snapshots from an EBS volume which is saved in S3
  - You can copy the snapshot to a different AZ and restore an EBS volume from that
- ELB (Elastic Load Balancing)
  - Distributes requests/traffic 
  - Spans Region, uses every AZ
  - Managed Service which is inherently secure, resilient and scalable
  - Health Check support
  - Integrates with Auto Scaling
  - Integrates with Route53
  - Offloads SSL, Customize Security Policy
  - 3 types of ELB:
    + Classic: Setup Ports to listen on, Register EC2 instance(s) and define which Port on the EC2 instance(s) to forward traffic to
    + Application Load Balancer: Setup Ports to listen on, Create Target Groups and then use Layer7 content filtering rules to route traffic ('/abc') to a specific Target Group. Allows Dynamic Port mapping so that one EC2 instance can receive traffic on different ports. Not possible with Classic LB.
    + Network Load Balancer: Setup Ports to listen on, Create Target Groups and then forward traffic to Ports on the Target Group. Why? Since NLB is a Layer3 Load Balancer. Handles very long running connections (for months) to backend Targets.
- S3 (Simple Storage Service)
  - Object Storage
  - Distributed K/V store
  - Buckets and Objects
  - Cluster spans Region
  - Durable to loss ot 2 AZs
  - Server side Encryption (AES256)
- S3 Use Cases
  - Static HTML
  - CSS, JavaScript
  - Images
  - Audio/Video files
  - PDF, eBooks
  - Software Downloads
  - Log Collection
  - Backups (EBS Snapshots)
  - Data Lakes
- CloudWatch
  - Why?
    + Intrumentation is key in Cloud
    + Are we over or under provisioned?
    + What is current demand/load?
    + Where are the bottlenecks - CPU, IO, etc?
    + Are any resources idle?
  - CloudWatch Monitoring
    + Collects Metrics
    + Stores Metrics for 2 Weeks
    + Accessible via API
    + Unique Metrics Set per Service
    + Custom Metrics ($/metric)
  - CloudWatch Logs
    - Collect logs by streaming
    - Search and filter using specific syntax
      + Create Metric Filters
        - Number of 404s
        - Bytes transfered 
        - Number of Exceptions
    - Configure an agent on EC2 instance to watch file(s)
    - Any appending events can be streamed
    - Collect Route53 DNS queries
    - Default retention indefinite
    - Can archive to Amazon S3
    - Stream to Amazon ElasticSearch
    - Process with Lambda  
  - Usage Examples
    - EC2 Metrics
      + Default 5 min interval
      + Detailed 1 min interval ($/instance)
      + Reported by Hypervisor
    - ELB Metrics
      + Default 1 min interval
      + Requests per min, Healthy Hosts, etc.
    - DynamoDB
      + Read/Write throughput, etc.
  - CloudWatch Alarms
    - Triggered based on breach of some threshold
    - Does not signal emergency
- Auto Scaling
  - Replace failed instances not just in the same AZ, but across AZs in a Region
  - Change capacity according to load (read, demand)
  - Maintain fixed size fleet
  - Works hand-in-hand with CloudWatch
  - Events
    + SNS
    + Lambda
  - Usages
    + Demand-based Auto Scaling
    + Reliable Apps
- CloudFront
  - Create a "distribution" (web or streaming)
  - Connect the distribution to one or more "origins"
  - Configure the "behaviors" of the "distribution" by configuring it 
    + To connect to the right origin (say, S3) if the request matches "/assets/*"
    + To connect to ELB and the Target Groups behind it for everything else ("/*")
  - Caches content at Edge Location
  - Supports static and dynamic content
  - You can customize the cache behavior
    + Set default TTL for static content
    + Set no TTL for dynamic content
  - Caching behavior can be changed on a per response basis
  - Custom DNS
  - Custom SSL
  - RTMP and HLS streaming
- Lambda
  - Serverless App Infrastructure
  - Use cases
    + Scheduled Tasks
    + Event Handlers
  - Pay for compute time per 100ms
  - Create functions
    + Online Editor
    + Upload Zip
  - Invoke functions
    + CLI or SDK
    + Events
    + Cron-style schedule
  - AWS Handles
    + Infrastructure
    + Deployment to necessary compute systems
    + Scaling
  - We specify
    + Runtime (Python, etc.)
    + Memory limit
    + Execution timeout
- RDS
  - Choice of
    + MySQL
    + SQL Server
    + Oracle
    + PostgreSQL
    + MariaDB
    + Amazon Aurora
  - Reduced Operational Burden
  - Team can focus on App (SQL Queries)
  - Benefits
    + Read Replicas
    + Automated
      - OS & DB Installation
      - OS Patches
      - DB Engine Minor Updates
      - Backups
      - Failover
  - Multi-AZ deployment
    - HA
    - Physically distinct servers
    - Automatic failover
      + Loss of Network
      + Compute failure
      + Storage failure
    - Production Best Practice
  - Backups
    - Performed once per day
    - You control backup window
    - Retained up to 35 days
    - Point-in-time restore
    - All backups are deleted along with deletion of RDS instance
  - Backups: Manual Snapshot
    - Performed at any time
    - Can copy to other regions
    - Retained indefinitely
  - Aurora
    - Compatible with
      + MySQL 5.6
      + Postgres 9.6
    - 3-5x performance increase
    - Storage up to 64TB
      + Auto-scaled
      + 6 copies across 3 AZs
    - Up to 15 Read Replicas
    - Aurora Multi-Master
    - Aurora Serverless
  - DB Migration
    - Dump and import
    - Backup/Restore
    - AWS DB Migration Service
      + Supports widely used DBs
      + Schema Conversion tool
      + Consolidate DBs
      + Heterogenous/Homegenous DBs
      + Continuous replication
- DynamoDB
  - NoSQL data store
  - Backed by SSD
  - Single-digit ms response
  - Built-in security, resilience
  - Replicated across numerous AZs in the Region
  - No limits to storage or throughput
  - Provisioned throughput (reads/sec or writes/sec)
  - Can auto-scale
  - Basics
    - Tables (Collections, Tables)
    - Items (Documents, Rows)
    - Attributes (Fields, Columns)
    - No joins or relationships. Translation: No foreign keys
    - Schema-less



## References

**Additional AWS Services**
- Developer Tools
  + CodeCommit: Think GitHub (Git portion)
  + CodeBuild: Run Compilation/CI on your code
  + CodeDeploy
  + CodePipeline: Wraps them all into a Pipeline
- Application Services
  + Step Functions
  + SWF (Simple Workflow Service)
  + API Gateway: Create, publish and Monitor APIs which routes request to business functionalities (like Lambda). Think doorway to accessing your backend services
  + AppStream
  + Elastic Transcoder: Changes video format to support different devices
- Analytics
  + Athena: Turning flat files (CSV) into databases with SQL query frontend
  + EMR (Elastic Map Reduce): Used to process large amounts of data! Using framework called Hadoop or Spark
  + Cloud Search: Fully managed AWS service
  + Elastic Search: Service using Elastic!
  + Kinesis: Streaming and analyzing realtime data. Example: Financial transaction analysis in realtime, social media stream analysis for sentiment analysis
  + Data Pipeline: Move data from S3 to DynamoDB, for example
  + Quick Sight: Business Analytics tool. Visualization tool. 
- AI
  + lex
  + polly: text into voice
  + machine learning: give the dataset and predict outcome based on the learning
  + rekognition: upload a pic and it will tell you what picture it is
- Mobile App Services
  + Cognito
  + Device Farm
  + Mobile Hub
  + Mobile Analytics
  + PinPoint: Think of combining Google Analytics with targeted marketing campaigns.
- Business Productivity
  + WorkDocs: Think Sharepoint
  + WorkMail: Think Exchange
- IoT
  + iOT
- Migration
  + Snowball: An appliance to migrate/transfer content from Enterprise to AWS
  + Snowball Edge
  + DMS (Database Migration Service): A service to migrate database from enterprises into AWS or within AWS regions or even across Database types
  + SMS (Server Migration Service): A service to migrate VMs


