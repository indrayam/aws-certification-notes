# AWS Certified Cloud Practitioner (CCP) 2020: My Notes

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
  + Cloud Watch: Monitor performance of things like EC2 (Disk Utilization, RAM Utilization etc.)
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
    - 10.2.0.0/21 can have a maximum of 2^11 - 2 = 2044 Hosts in the Subnet
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
    - Performance

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


