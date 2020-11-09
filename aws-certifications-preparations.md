# AWS Certifications Preparations

## AWS Certifications
- AWS Certified Cloud Practitioner ✅
- AWS Certified Solutions Architect - Associate
- AWS Certified SysOps Administrator - Associate
- AWS Certified Developer - Associate
- AWS Certified Advanced Networking - Specialty

## AWS Certified Solutions Architect - Professional
- [acloud.guru: AWS Certified Solutions Architect - Professional 2020](https://acloud.guru/learn/aws-certified-solutions-architect-professional?_ga=2.211328726.2113966801.1601496229-472653352.1600688128)
- [Dieter Matzion: Managing Cloud Costs **Oct 2019**](https://learning.oreilly.com/live-training/courses/managing-cloud-costs/0636920321736/)
- [Chad Smith: AWS Account Setup Best Practices **May 2019**](https://learning.oreilly.com/live-training/courses/aws-account-setup-best-practices/0636920266549/)
- [Richard Jones: AWS From Basics to Advanced **Dec 2017**](https://learning.oreilly.com/learning-paths/learning-path-amazon/9780135116548/?autoplay=false)

## AWS Certified DevOps Engineer - Professional
- [Richard Jones: Automation in AWS with CloudFormation **2017**](https://learning.oreilly.com/videos/automation-in-aws/9780134818313?autoplay=false)
- [Richard Jones: AWS CloudFormation Deep Dive **April 2019**](https://learning.oreilly.com/live-training/courses/aws-cloudformation-deep-dive/0636920252399/)
- [Chad Smith: AWS Monitoring Strategies **Sept 2020**](https://learning.oreilly.com/live-training/courses/aws-monitoring-strategies/0636920411703/)
- [Richard Jones: Deploying Container-Based Microservices on AWS **Mar 2019**](https://learning.oreilly.com/live-training/courses/deploying-container-based-microservices-on-aws/0636920238485/)
- [Vallard Benin: Kubernetes on AWS **Feb 2020**](https://learning.oreilly.com/live-training/courses/kubernetes-on-aws/0636920359586/)
- [Designing Serverless Architecture with AWS Lambda **April 2019**](https://learning.oreilly.com/live-training/courses/designing-serverless-architecture-with-aws-lambda/0636920263869/)

## AWS Networking Specialty Certification
- Book: AWS Certified Advanced Networking Official Study Guide (Chauhan, Devine, etc.)
- [IP Subnetting: From Beginning to Mastery](https://learning.oreilly.com/live-training/courses/ip-subnetting-from-beginning-to-mastery/0636920390091/)
- [Richard Jones: Networking in AWS **2017**](https://learning.oreilly.com/videos/networking-in-amazon/9780134850849?autoplay=false) 
- [Michael Shannon: AWS Networking Essential June **2020**](https://learning.oreilly.com/live-training/courses/aws-networking-essentials/0636920407546/)
- [Chad Smith: AWS Network Certification GitHub Repo](https://github.com/arpcefxl/aws-network-certification)

## AWS Services for all Associate Level Certifications

### 1. AWS and/or Architecture Concepts
- Well Architected Framework
- Shared Responsibility Model
- HTTP Protocol

### 2. Identity & Access
+ AWS IAM ✅
  + IAM policies and roles
  + Cross account access
  + Multi-factor authentication (MFA)
  + API calls
  + IAM Roles with EC2 (instance profiles)
  + Access keys vs roles
  + IAM best practices
  + Federation
+ AWS Organizations ✅

### 3. Networking
+ VPC ✅
+ Elastic Load Balancing (ELB) ✅
+ Route53 ✅
+ CloudFront ✅
  + Viewer vs origin protocol policies
  + Lambda@Edge use cases
  + Invalidate cache
  + Signed URLs / cookies
+ Amazon API Gateway
  + Lambda / IAM / Cognito authorizers
  + Invalidation of cache
  + Integration types: proxy vs custom / AWS vs HTTP
  + Caching
  + Import / export OpenAPI Swagger specifications
  + Stage variables
  + Performance metrics
+ AWS App Mesh
+ AWS Transit Gateway
+ AWS Global Accelerator

### 4. Compute & Containers
+ EC2 ✅
+ ASG ✅
+ Elastic Block Store (EBS) ✅
+ AWS Elastic Container Service (ECS) 🚧
  + Shared storage between containers
  + Single vs multi-docker environments
  + Uploading / downloading images with ECR
  + Placement strategies (e.g. spread, binpack, random etc.)
  + Port mappings
  + Defining task definitions
  + IAM Roles for Tasks
+ AWS Elastic Kubernetes Service (EKS) 🚧
+ AWS Lambda
  + Invocation types
  + Using notifications and event source mappings
  + Concurrency and throttling
  + X-Ray and Amazon SQS DLQs
  + Versions and aliases
  + Blue/green deployment
  + Packaging and deployment
  + VPC connections (with Internet/NAT GW)
  + Lambda as ELB target
  + Dependencies
  + Environment variables (inc. encrypting them)
+ AWS Fargate 🚧
+ AWS Beanstalk
  + Deployment policies and blue/green
  + .ebextensions and config file usage
  + Updating deployments
  + Worker vs web tier
  + Deployment, packaging and files, code, commands used
  + Use cases

### 5. Storage
+ Amazon Simple Secure Storage (S3) ✅
  + Encryption – make sure you understand S3 encryption very well for the exam!
  + S3 Transfer Acceleration
  + Versioning
  + Copying data
  + Lifecycle rules
+ Amazon Elastic File System (EFS)
+ Amazon S3 Glacier & S3 Glacier Deep Archive

### 6. Database
+ RDS Aurora
+ Amazon DynamoDB
  + Scans vs queries (and the APIs, parameters you can use)
  + Local and Global Secondary indexes
  + Calculating Read Capacity Units (RCUs) and Write Capacity Units (WCUs)
  + Performance / optimization  best practices
  + Use cases (e.g. session state, key/value data store, scalability)
  + DynamoDB Streams
  + Use in serverless app with Lambda and API Gateway
  + DynamoDB Accelerator (DAX) use cases
+ Amazon ElastiCache (Redis)
  + Use cases (caching and session state)
  + In-memory data store
  + Services it sits in front of (e.g. Amazon RDS)
  + Comparison against DynamoDB DAX
  + Lazy loading vs Write Through Caching
  + Memcached vs Redis

### 7. App Integration
+ Amazon Simple Notification Service (SNS)
+ Amazon Simple Queue Service (SQS)
  + Standard queues, FIFO, DLQ, delay queue
  + Decoupling applications use cases
  + Event source mapping to Lambda
  + Visibility timeout
  + Short polling vs long polling
+ AWS Step Functions
  + Step Functions state machines
  + Using to coordinate multiple Lambda function invocations

### 8. Analytics
+ Amazon Kinesis
+ Apache EMR
+ Amazon RedShift

### 9. Developer Tools
+ CodeStar
+ Cloud9
+ CodeCommit ✅
+ CodeBuild ✅
+ CodeArtifact
+ AWS Elastic Container Registry (ECR) ✅
+ CodeDeploy ✅
+ CodePipeline ✅
  + Know how each tool fits into the CI/CD pipeline
  + Various files used such as appspec.yml, buildspec.yml etc.
  + Process for packaging and deployment
  + Deployment types with CodeDeploy including different destination services (e.g. Lambda, ECS, EC2)
  + Manual approvals with CodePipeline
+ AWS AppConfig
+ AWS XRay
  + X-Ray daemon, installing and configuring
  + Lambda with X-Ray
  + Use cases / benefits
  + Inclusion in Elastic Beanstalk environment
  + Annotations vs segments vs subsegments vs metadata
  + API calls
  + Port used (UDP 2000)

### 10. Security 
+ AWS Certificate Manager ✅
+ AWS Secrets Manager
+ AWS Key Management Service (KMS)

### 11. Management
+ CloudWatch
  + Monitoring application logs
  + Trigger scheduled Lambda invocation
  + Custom metrics
  + Metric resolution
+ CloudTrail
+ AWS Systems Manager
+ CloudFormation ✅
  + CloudFormation template anatomy (e.g. mappings, outputs, parameters, etc.)
  + Packaging and deployment including commands used
  + AWS Serverless Application Model (SAM)
+ Resource Groups & Tag Editor ✅
+ Trusted Advisor ✅
+ Control Tower
+ Personal Health Dashboard

### 12. Cost Management
+ AWS Cost Explorer ✅
+ AWS Budgets ✅

### 13. Miscellaneous
+ Cognito
  + User pools vs Identity pools
  + Unauthenticated identities
  + AWS Cognito Sync
  + Using MFA with Cognito
  + Web identity federation
+ Athena
+ Macie
