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


