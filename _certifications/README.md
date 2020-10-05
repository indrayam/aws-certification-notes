# Getting AWS Certifications: My Notes

- AWS Certified Cloud Practitioner
- AWS Certified Solutions Architect - Associate
- AWS Certified SysOps Administrator - Associate
- AWS Certified Developer - Associate
- AWS Certified Advanced Networking - Specialty

## Getting AWS Certified (Current Progress)

### Preparing for CCP
- [acloud.guru: Introduction to AWS](https://learn.acloud.guru/course/aws-technical-essentials/dashboard) 🚧
- [Richard Jones: AWS Certified Cloud Practitioner, 1/e **May 2019**](https://learning.oreilly.com/learning-paths/learning-path-aws/9780135940037/?autoplay=false)
- [Michael Shannon: AWS Certified Cloud Practitioner Exam Crash Course **May 2019**](https://learning.oreilly.com/live-training/courses/aws-certified-cloud-practitioner-exam-crash-course/0636920260257/)
- [IP Subnetting: From Beginning to Mastery](https://learning.oreilly.com/live-training/courses/ip-subnetting-from-beginning-to-mastery/0636920390091/)
- [acloud.guru: AWS Certified Cloud Practitioner 2020](https://learn.acloud.guru/course/aws-certified-cloud-practitioner/dashboard)
- [freeCodeCamp: AWS Certified Cloud Practitioner Training 2020 - Full Course **Oct 2019**](https://www.youtube.com/watch?v=3hLmDS179YE)


### AWS Services to Peruse
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

---

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

## Getting AWS Certified (Learning)

### Projects
- AWS The Good Parts
- Manning LiveProject: [Automating Infrastructure for an E-commerce Website with Terraform and AWS
](https://www.manning.com/liveproject/automating-infrastructure-for-an-e-commerce-website-with-terraform-and-aws)
- Manning LiveProject: [Secure Business Infrastructure with Your Own VPN](https://www.manning.com/liveproject/secure-business-infrastructure-with-a-custom-vpn)
- Manning LiveProject: [Creating a WhatsApp Notification Service Using AWS Lambda and a Serverless Framework](https://www.manning.com/liveproject/creating-a-whatsapp-notification-service-using-aws-lambda-and-a-serverless-framework)
- [Github: AWS Boilerplate](https://github.com/apptension/aws-boilerplate)

### Books
- AWS The Good Parts
- AWS Security
- AWS in a Month of Lunches
- AWS in Action 2nd Ed
- [The Definitive Guide to AWS Application Integration: With Amazon SQS, SNS, SWF and Step Functions](https://learning.oreilly.com/library/view/the-definitive-guide/9781484254011/)
- [Ben Piper & David Clinton: AWS Certified Cloud Practitioner Study Guide **July 2019**](https://learning.oreilly.com/library/view/aws-certified-cloud/9781119490708/)
- [AWS Certified Solutions Architect Official Study Guide **Oct 2016**](https://learning.oreilly.com/library/view/aws-certified-solutions/9781119138556/)
- [AWS Certified Solutions Architect Practice Tests **Mar 2019**](https://learning.oreilly.com/library/view/aws-certified-solutions/9781119558439/)
- [AWS Certified Developer Official Study Guide, Associate Exam **Sep 2019**](https://learning.oreilly.com/library/view/aws-certified-developer/9781119508199/)

### VoD
- [acloud.guru: Introduction to AWS](https://learn.acloud.guru/course/aws-technical-essentials/dashboard)
- [acloud.guru: AWS Certification Preparation Guide](https://learn.acloud.guru/course/aws-certification-preparation/dashboard)
- [Richard Jones: Getting Started with Amazon Web Services (AWS) **Mar 2019**](https://learning.oreilly.com/live-training/courses/getting-started-with-amazon-web-services-aws/0636920237099/)
- [AWS Training](https://www.aws.training/)
- [edX AWS Courses](https://courses.edx.org/dashboard)

## AWS Certified Cloud Practitioner
- [acloud.guru: AWS Certified Cloud Practitioner 2020](https://learn.acloud.guru/course/aws-certified-cloud-practitioner/dashboard)
- [freeCodeCamp: AWS Certified Cloud Practitioner Training 2020 - Full Course **Oct 2019**](https://www.youtube.com/watch?v=3hLmDS179YE)
- [Richard Jones: AWS Certified Cloud Practitioner, 1/e **May 2019**](https://learning.oreilly.com/learning-paths/learning-path-aws/9780135940037/?autoplay=false)
- [Michael Shannon: AWS Certified Cloud Practitioner Exam Crash Course **May 2019**](https://learning.oreilly.com/live-training/courses/aws-certified-cloud-practitioner-exam-crash-course/0636920260257/)

## AWS Certified Solutions Architect - Associate
- [acloud.guru: AWS Certified Solutions Architect Associate SAA-C02](https://learn.acloud.guru/course/aws-certified-solutions-architect-associate/dashboard)
- [acloud.guru: Well Architected Framework](https://learn.acloud.guru/course/aws-well-architected-framework/dashboard)
- [Article: Tips from my Journey to an AWS Solutions Architect Associate Certification](https://medium.com/@lior.k.sh/tips-from-my-journey-for-aws-solutions-architect-associate-certification-8f4eb8344a98)
- [Chad Smith: AWS Certified Solutions Architect - Associate (SAA-C02) **2020**](https://learning.oreilly.com/videos/aws-certified-solutions/9780136721246)
- [freeCodeCamp: AWS Certified Solutions Architect - Associate 2020 (PASS THE EXAM!) **Dec 2019**](https://www.youtube.com/watch?v=Ia-UEYYR44s&feature=youtu.be)
- [Richard Jones: Learning Path: AWS Certified Solutions Architect (Associate), 1/e **Apr 2019**](https://learning.oreilly.com/learning-paths/learning-path-aws/9780135944769/)
- [Richard Jones: AWS Certified Solutions Architect Associate Crash Course **Oct 2019**](https://learning.oreilly.com/live-training/courses/aws-certified-solutions-architect-associate-crash-course/0636920319108/)
- [Mark Wilkins: AWS Design Fundamentals **April 2019**](https://learning.oreilly.com/live-training/courses/aws-design-fundamentals/0636920251668/)
- [Richard Jones: AWS Certified Solutions Architect Associate Crash Course **May 2019**](https://learning.oreilly.com/live-training/courses/aws-certified-solutions-architect-associate-crash-course/0636920273509/)
- [AWS Training: Exam Readiness: AWS Certified Solutions Architect – Associate](https://www.aws.training/Details/eLearning?id=20686)

## AWS Certified Developer - Associate
- [acloud.guru: AWS Certified Developer Associate 2020](https://learn.acloud.guru/course/aws-certified-developer-associate/dashboard)
- [Nick Garner: AWS Certified Developer Associate Crash Course **Sep 2020**](https://learning.oreilly.com/live-training/courses/aws-certified-developer-associate-crash-course/0636920447825/)
- [Nick Garner: AWS Certified Developer (Associate) **2019**](https://learning.oreilly.com/videos/aws-certified-developer/9780134855158)
- [AWS Training: Exam Readiness: AWS Certified Developer – Associate (Digital)](https://www.aws.training/Details/Curriculum?id=19185)

## AWS Certified SysOp Administrator - Associate
- [acloud.guru: AWS Certified SysOps Administrator Associate 2020](https://acloud.guru/learn/aws-certified-sysops-administrator-associate?_ga=2.211328726.2113966801.1601496229-472653352.1600688128)
- [AWS Training: Exam Readiness: AWS Certified SysOps Administrator - Associate](https://www.aws.training/Details/Video?id=27486)

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
- [IP Subnetting: From Beginning to Mastery](https://learning.oreilly.com/live-training/courses/ip-subnetting-from-beginning-to-mastery/0636920390091/)
- [Richard Jones: Networking in AWS **2017**](https://learning.oreilly.com/videos/networking-in-amazon/9780134850849?autoplay=false) 
- [Michael Shannon: AWS Networking Essential June **2020**](https://learning.oreilly.com/live-training/courses/aws-networking-essentials/0636920407546/)
- [Chad Smith: AWS Network Certification GitHub Repo](https://github.com/arpcefxl/aws-network-certification)

