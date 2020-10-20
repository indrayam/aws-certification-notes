# acloud.guru: AWS Certified Cloud Practitioner 2020 Notes

## Exam Blue Print
- Concepts (26%)
- Security (25%)
- Technology (33%)
- Billing & Pricing (16%)

## Cloud Concepts & Technology

### 6 Advantages of Cloud
- Trade Capital expense for Variable Expense
  + Stop spending money running and maintaining DCs
- Go global in minutes!
- Stop guessing about capacity
- Increase speed and agility
- Benefit from massive economies of scale

### Types of Cloud Computing
- IaaS (For example: EC2)
- PaaS (For example: Heroku, Lightsail, Elastic Beanstalk)
- SaaS (For example: Gmail)

### Types of Cloud Computing Deployments
- Public Cloud: AWS, Azure, GCP
- Hybrid: Mix of Public and Private
- Private (On-Premise): You manage it in your DC using Openstack or VMWare

## AWS Services - Cloud Practitioner Scope
- AWS Global Infra
- Security, Identity & Compliance
- Compute
  + EC2 
  + Lambda
- Network & Content Delivery
  + VPC
  + Route53
- Storage
  + S3
  + Glacier
- Databases
  + RDS
  + DynamoDB
- AWS Cost Management
- Migration & Transfer

## Exam Tips: Why choose an AWS Region?
- Data Sovereignty Laws
- Latency to end users
- AWS Services

## Exam Tips: Support Plans
- Basic: Free
- Developer: 
  + Starts at $29/month and scales up based on usage
  + 12-24 hour response time during local business hours for Support Cases
- Business: 
  + Starts at $100/month and scales up based on usage
  + 1 hr response time for urgent Support Cases
  + Full Access to AWS Trusted Advisor for optimizing your AWS Infrastructure
  + Access to AWS Support APIs for automating your support cases and retrieving Trusted Advisor results
- Enterprise:
  + Starts at $15,000/month and scales up based on usage
  + 15 min response time for critical Support Cases and prioritized case handling
  + Full Access to AWS Trusted Advisor for optimizing your AWS Infrastructure
  + Access to AWS Support APIs for automating your support cases and retrieving Trusted Advisor results
  + Access to Technical Account Manager (TAM) who provides proactive guidance and best practices to help plan, develop and run AWS
  + Access to Support Concierge who provides Billing and Account analysis and assistance
  + Access to Infra Event Management to support product launches, seasonal promotions/events and migrations

## Exam Tips: AWS IAM
- IAM is not tied to a specific Region. It is a Global service.
- Access AWS Platform using:
  + Console
  + CLI
  + SDK
- "root" account is the email address you used to setup your AWS account. It has FULL ADMIN privileges
- Do not use "root" account for day-to-day use. Neither should the "root" account credentials be shared with anyone
- Enable MFA for the "root" user
- Create separate account for users. Assign them tp Groups.
- Users will inherit the permissions of the Group(s) that they belong to
- To set permissions in a Group, you need to apply "Policy" to that Group.
- Policies are internally represented as JSON doc

## Exam Tips: S3
- Files in S3 can be from 0 Bytes to 5 TB
- Unlimited storage
- Files are stored in "Buckets"
- "Bucket" names is a Universal namespace.
- S3 is Object based. Object consists of:
  + Key (Name of the object)
  + Value (The file)
  + Version ID
  + Metadata
  + Subresources:
    - ACL
    - Torrent
- Data Consistency in S3
  + Read after Write Consistency for PUTS of new Object
    - Translation: If you write a new file and read it immediately afterwards, you will be able to view that data
  + Eventual Consistency for overwrite PUTS and DELETES (can take some time propogate)
    - Translation: If you update an EXISTING file or delete a file and read it immediately afterwards, you may get an older version or you may not. Basically, changes to objects can take a little bit of time to propogate
- S3 is built for 99.99% availability. However, Amazon will guarantee 99.9% availability
- S3 durability is 11x9s.
- S3 Features:
  + Tiered Storage
    - Standard
    - S3 - Infrequently Accessed
    - S3 One Zone - Infrequently Accessed
    - S3 - Intelligent Tiering 
    - S3 Glacier (Data Archiving): Retrieval time from minutes to hours.
    - S3 Glacier Deep Archive: Absolute lowest cost where retrieval time of 12 hours is acceptable
    - S3 Outposts is a storage class to deliver object storage to on-premises AWS Outpost environments
  + Lifecycle Management
  + Versioning
  + Encryption
  + Secure your data using ACLs and Bucket Policies
    - ACLs are at File level
    - Bucket Policies control access at "Bucket" level
- S3 Charges
  + Storage Size on a per Gig bases
  + Storage Management Pricing 
  + Number of Requests
  + Data Transfer Pricing
  + Transfer Acceleration
    - Takes advantage of CloudFront's globally distributed edge locations
    - When a user uploads a file to a Bucket with Transfer Acceleration enabled, content is uploaded to the nearest Edge location and then is "beamed" to the actual S3 bucket in the appropriate Region using Amazon's Networking backbone as opposed to traversing over the public Internet
  + Cross Region Replication
    - File gets replicated automatically to another Region
- S3 is Object based, not Block based. So, not suitable for installing OS.
- S3 buckets can be viewed globally. However, when you upload it, you do upload it to a Region. Or at least you can
- Btw, you can change Storage Class and Encryption settings of your object on-the-fly
- Access Control
  + Bucket Policies (All files inside the Bucket)
  + Object Policies (Individual files)
  + IAM Policies to Users & Groups
- You can use S3 to host static websites, but not dynamic sites. For example, sites running on Wordpress.
- S3 scales automatically to meet your demand. Many enterprises put static websites on S3 when they think there is going to be a large number of requests.

## Exam Tips: CloudFront
- AWS CDN
- CDN is a system of distributed servers that deliver webpages and other web content to a user based on:
  + geographical location of the user
  + the origin of the web page
  + content delivery server
- Terminology
  + Distribution - Collection of Edge Locations
  + Edge Location - This is the location where content will be cached. This is separate from AWS Region/AZs
  + Origin - This is the origin (or source) of all files that the CDN will distribute. This can be an S3 bucket, an EC2 instance, an Elastic Load Balancer or Route53
- Objects are cached for TTL seconds. By default TTL is 48 hrs (86440 secs)
- 2 Types of Distributions
  + Web Distribution (for Website Streaming)
  + RTMP Distribution (for Media Streaming)
- Edge Locations are not just for READ only. You can write to them as well, as we saw with Transfer Acceleration property of an S3 object
- You can clear your cached objects, but you will be charged

## Exam Tips: EC2
- Virtual server(s) in the cloud!
- Pricing Model
  + On-demand. Pay by the sec. 
    - No upfront payment or long-term commitment
    - Good for short-term, spik, or unpredictable workloads that cannot be interrupted
    - Apps being developed or tested on EC2 for the first time
  + Reserved. Provides you with a capacity reservation and at a heavy discount. Contract terms are 1 year or 3 years.
    - Apps with steady state or predictable usage
    - Users willing to make upfront payments to reduce their total computing costs even further
    - Apps with unique capacity needs that they would rather reserve beforehand
    - Types
      - Standard (75%)
      - Convertible Reserved Instances (54%)
      - Scheduled Reserved Instances: This allows you to match your capacity reservation to a predictable recurring schedule that only requires a fraction of the day, week or month
  + Spot. Enables you to bid for the server
    - Apps with flexible start or end time
    - Apps that are only feasible at very low compute prices (like genomics etc.)
    - Users with urgent computing needs for large amounts of additional capacity. Only if the spot price is below on-demand instance.
  + Dedicated Hosts. Physical EC2 server dedicated for your use. Dedicated hosts can help you reduce costs by allowing you to use your existing server-bound licenses. Quite rare.
    - Useful for regulatory requirements that may NOT support multi-tenant virtualization
    - Great for hosting software which DOES NOT support multi-tenancy or cloud deployments
    - Can be purchased on-demand (hourly)
- EC2 Instance Types
  + ARM-based => A (scale out workloads such as web servers)
  + General purpose => T (Lowest Cost, Small Web Servers/DB), M (App Servers)
  + Field Programmable Gate Array (FPGA) => F
  + Graphics Intensive, Machine Learning, Bitcoin Mining etc. => G, P (GPU)
  + Compute Optimized => C
  + Memory Optimized => R, X (SAP Hana, Spark)
  + Disk IO Throughput => I, H
  + Dense Storage => D (Fileservers, Hadoop)
  + High Compute Capacity & High Memory Footprint => Z
  + Bare Metal => U
- EC2 Instance Types - Mnemonic
  + F = FPGA
  + I = IOPS
  + G = Graphics
  + H = High-Disk throughput
  + T = Cheap (think, t2.micro)
  + D = Density
  + R = RAM
  + M = Main choice for general purpose apps
  + C = Compute
  + P = Pix (Graphics)
  + X = Xtreme Memory
  + Z = Xtreme Memory and CPU
  + A = ARM based workloads
  + U = Bare Metal
Stands for, "FIGHT DR MCPXZ in AUstin"
- EBS
  + Virtual hard disks
  + EC2 instance needs to be in the same AZ as EBS for it to be able to mount the EBS volume
  + SSD Types
    - GP2 (General Purpose): Balances price and performance for a wide variety of workloads
    - Provisioned IOPS SSD  (IO1): Highest-performance SSD volume for mission-critical low-latency or high-throughput workloads
  + Magnetic Types
    - Throughput Optimized HDD (ST1): Low cost HDD volume designed for frequently accessed, throughput-intensive workloads
    - Cold HDD (SC1): Lowest cost HDD volume designed for less frequently accessed workloads (File Servers)
- If the Spot instance is terminated by Amazon EC2, you will NOT be charged for the partial hour of usage. However, if you terminate the instance yourself, you will be charged for the hour in which the instance ran