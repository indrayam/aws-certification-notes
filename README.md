# AWS Architecture

## AWS Online Docs & References
- [AWS Architecture Center](https://aws.amazon.com/architecture/?awsf.quickstart-architecture-page-filter=highlight%23new) 🚧
- [AWS Well Architected](https://aws.amazon.com/architecture/well-architected/?achp_wa1&wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)
- AWS Well Architected Tool
- [AWS Archirecture Monthly](https://aws.amazon.com/whitepapers/kindle/?icmpid=link_from_docs_website)
- [AWS Hands-On Tutorials](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23compute%7Ccategory%23databases)
- [AWS Quick Starts](https://aws.amazon.com/quickstart/?quickstart-all.sort-by=item.additionalFields.sortDate&quickstart-all.sort-order=desc)
- [AWS Free Digital Training](https://www.aws.training/LearningLibrary?filters=language%3A1&filters=digital%3A1&tab=view_all)
- [AWS Workshops](https://awsworkshop.io/)
  + [AWS Security Workshops](https://awssecworkshops.com/)
  + [AWS Global Accelerator Workshop](https://intro-to-global-accelerator.workshop.aws/)
- [AWS Whitepapers & Guides](https://aws.amazon.com/whitepapers/?icmpid=link_from_docs_website&whitepapers-main.sort-by=item.additionalFields.sortDate&whitepapers-main.sort-order=desc)

## AWS App Architecture Samples
![AWS Example Architecture v1](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v1.jpg)

![AWS Example Architecture v2](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v2.jpg)

![AWS Example Architecture v3](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v3.jpg)

# AWS Services

## Part 0: Best-Practice/Cost Optimization Enablers
- [AWS Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html) 🚧
- [AWS Pricing Calculator](https://calculator.aws/#/) 🚧
- [AWS Quick Starts](https://aws.amazon.com/quickstart/?quickstart-all.sort-by=item.additionalFields.sortDate&quickstart-all.sort-order=desc) 🚧
- [AWS Compliance](https://aws.amazon.com/compliance/) 🚧
- AWS Trusted Advisor 🚧

## Part 1: Getting Started with AWS
- AWS Identity & Access Management (IAM)
  + AWS Organizations 🚧
  + Users: Root Account, IAM Users, MFA, Access Key ID, Secret Access Key ✅
  + Groups ✅
  + Roles 🚧
  + Permissions via Identity and Resource Policies 🚧
  + AWS Control Tower
    - [AWS Landing Zone](http://aws.amazon.com/answers/aws-landing-zone/)
  + *Amazon Cloud Directory*
  + *Amazon Directory Service*
  + *AWS Single Sign-On*
- Billing Dashboard for Cost Management
  + AWS Budgets 🚧
  + AWS Cost Explorer 🚧
  + AWS Cost and Usage Reports
  + Reserved Instance Reporting
  + Tag Editor 🚧
+ Network/Security
  - VPC ✅
    + 1 Region, 3 AZs ✅
    + "N" Subnets (Public/Private) ✅
    + Security Groups ✅
    + RouteTable ✅
    + Internet Gateway ✅
    + NAT Gateway
    + NACL ✅
    + VPC Endpoint
    + VPC Endpoint Services (AWS PrivateLink)
    + Elastic IP (EIP)
  - Route53 ✅
  - CloudFront ✅
  - Amazon API Gateway
  - AWS App Mesh
  - AWS Cloud Map
  - *AWS Transit Gateway* (think, Cisco SCI) 🚧
  - *AWS Direct Connect*
  - *AWS Global Accelerator*
+ Compute: Virtual Machines
  - EC2 ✅
    + Ubuntu 20.04 AMI ✅
    + Amazon Linux 2 AMI ✅
    + Elastic Block Store (EBS) ✅
    + Auto Scaling ✅
      - Launch Configs ✅
      - Auto Scaling Groups ✅
  - Elastic Load Balancing (ELB) 🚧
    + Application Load Balancing (ALB) ✅
      - Target Groups
    + Network Load Balancing (NLB) 🚧
+ Compute: PaaS, CaaS, FaaS 
  - AWS Elastic Container Service (ECS)
    + AWS Elastic Container Registry (ECR)
  - AWS Fargate
  - AWS Elastic Kubernetes Service (EKS)
  - AWS Lambda 🚧
  - *AWS Elastic Beanstalk*
  - *Amazon Lightsail* (v. DigitalOcean)
  - AWS Batch
+ Storage: Files
  - Amazon Simple Secure Storage (S3) ✅
  - Amazon Elastic File System
  - *Amazon S3 Glacier & S3 Glacier Deep Archive*
  - AWS Storage Gateway (Hybrid storage service that enables your on-premises apps to seamlessly use AWS cloud storage)
+ Data
  - RDS 🚧
    + Aurora/MySQL
    + Aurora/Postgres
    + Postgres
    + MySQL 🚧
  - Amazon DynamoDB
  - Amazon ElastiCache (Redis)
  - *Amazon Neptune*
  - *Amazon Quantum Ledger Database (QLDB)*
  - *Amazon Timestream*
  - *Amazon DocumentDB (MongoDB compatibility)*
+ Event-based Apps
  - Amazon Simple Notification Service (SNS)
  - Amazon Simple Queue Service (SQS)
    + 3Amazon MQ (Managed Apache ActiveMQ service)
  - AWS Step Functions (Workflow Engine, vs. Airflow, Argo)
    + AWS Simple Workflow Service (SWF)

## Part 2: DevSecOps

- Dev**Ops**
  - Amazon CloudWatch
    + Monitoring 🚧
    + Logs
    + Alarms
  - AWS Systems Manager
    + Resource Groups 🚧
    + Insights Dashboard
      - Pull API call logs from CloudTrail
      - Resource Config Changes, Software Inventory and Path Compliance status from AWS Config
      - Integrate AWS CloudWatch dashboards
      - AWS Trusted Advisor notifications
      - AWS Personal Health Dashboard performance and availability alerts
    + RunCommand
    + State Manager
    + Parameter Store
    + Session Manager
  - AWS X-Ray
  - AWS Auto Scaling
  - CloudFormation
  - CloudTrail
  - AWS Config
  - *AWS Opsworks*
    + Chef
    + Puppet 
  - AWS Service Catalog
  - Personal Health Dashboard
  - AWS License Manager
- **Dev**Ops
  - CodeCommit 🚧
  - CodeBuild 🚧
  - CodeArtifact
  - CodePipeline 🚧
  - CodeDeploy 🚧
+ Security & Compliance
  - AWS Security Hub
  - AWS Certificate Manager ✅
  - AWS WAF
    + AWS Firewall Manager
  - AWS Shield
    + Standard
    + Advanced
  - AWS Inspector
    + Extremely EC2 specific
  - Amazon GuardDuty
  - AWS Macie
  - AWS Secrets Manager (v. Vault)
  - AWS Key Management Service (KMS)
  - AWS CloudHSM (Hardware Security Module)
  - AWS Artifact

## Part 3: Big Data & BI Analytics
- *Amazon Athena* (SQL on S3)
- *Amazon EMR* (Managed Hadoop Framework)
  + Hadoop
  + Spark
  + HBase
  + Presto
  + Flink
- *Amazon CloudSearch*
- Amazon Elasticsearch
- Amazon Kinesis (Distributed Commit log for Streaming/Processing Data; vs. Kafka/Kafka Streams/kSQL)
  + Kinesis Data Firehose
  + Kinesis Data Streams
  + Kinesis Data Analytics
  + *Kinesis Video Streams*
  + Amazon Managed Streaming for Kafka (MSK)
- *Amazon Redshift (Data Warehouse; vs. BigQuery or Snowflake)*
- *Amazon QuickSight* (Business Intelligence Service; vs. Tableau, Microsoft Power BI)
- *AWS Glue* (Managed Extract Transform and Load (ETL) Service, vs. Informatica)
- *AWS Data Pipeline* (Movement and Transformation of data)
- *AWS Lake Formation* (Data Lakes, vs. Snowflake)

## Part 4: Software 2.0

### Artifical Intelligence
- AWS SageMaker
  + AWS SageMaker Ground Truth
- Amazon Comprehend (NLP service that uses machine learning to find insights and relationships in text)
- Amazon Lex (Build conversational interfaces into any app using voice and text. Speech recognition and natural language understanding are some of the most challenging problems to solve in computer science. Lex brings Alexa's tech!)
- Amazon Polly (Service that turns text into lifelike speech! Lets you create apps that talk!!)
- Amazon Rekognition (Service that makes it easy to add image analysis to apps)
- Amazon Translate (Machine Translation service that delivers fast, high-quality, and affordable language translation)
- Amazon Transcribe (Automatic Speech Recognition (ASR) service. Makes it easy for developers to speech-to-text capability to apps)
- Amazon Textract (Service that automatically extracts data from scanned docs. Goes beyond OCR to read data from form fields and tables)
- Amazon Forecast (Service that uses machine learning to deliver high quality accurate business forecasts)
- Amazon Personalize (Service that uses machine learning to help apps create individualized recommendations for their users/customers) 
- Amazon Deep Learning AMIs (Helps ML practitioners by giving them infra/tools to accelerate deep learning in the cloud)
- AWS DeepLens (Helps developers get started with Deep Learning)
- AWS DeepRacer (Helps developers get started with reinforcement learning(RL))
- Apache MXNet on AWS
- TensorFlow on AWS
- Amazon Elastic Inference (Allows you to attach low-cost GPU-powered acceleration to Amazon EC2 and SageMaker instances to reduce cost of running deep learning inference)
- AWS Inferentia (Machine Learning inference chip designed to deliver high performance at low cost. Making predictions using a trained machine learning model - a process called "inference" - can drive as much as 90% of the compute costs of the app. While Amazon Elastic Inference can reduce costs by up to 75%, some inference workloads require an entire GPU or have extremely low latency requirements. Solving this at low cost requires a dedicated inference chip!) 

### Robotics
- AWS Robomaker (Service that makes it easy to develop, test and deploy intelligent robotics apps)

### Satellite
- AWS Ground Station (Fully managed service that lets you control satellite communications, downlink and process satellite data etc.)

# Mastering AWS

## Mastering AWS: Books
- AWS in a Month of Lunches (Manning)
- AWS Security (Manning - EAP)
- AWS in Action 2nd Ed (Manning)
- AWS The Good Parts (Gumroad)
- AWS Certified Cloud Practitioner Study Guide (Ben Piper & David Clinton)
- AWS Certified SysOps Administrator Official Study Guide (Cole, Digby, etc.)
- AWS Certified Developer Official Study Guide (Alteen, Fisher, etc.)
- AWS Certified Advanced Networking Official Study Guide (Chauhan, Devine, etc.)

## Mastering AWS: VoDs
- AWS in Motion (Manning)
- [Richard Jones: Getting Started with Amazon Web Services (AWS) **Mar 2019**](https://learning.oreilly.com/live-training/courses/getting-started-with-amazon-web-services-aws/0636920237099/)

## Mastering AWS: Projects
- AWS The Good Parts ✅
- Manning LiveProject: [Automating Infrastructure for an E-commerce Website with Terraform and AWS
](https://www.manning.com/liveproject/automating-infrastructure-for-an-e-commerce-website-with-terraform-and-aws)
- Manning LiveProject: [Secure Business Infrastructure with Your Own VPN](https://www.manning.com/liveproject/secure-business-infrastructure-with-a-custom-vpn)
- Manning LiveProject: [Creating a WhatsApp Notification Service Using AWS Lambda and a Serverless Framework](https://www.manning.com/liveproject/creating-a-whatsapp-notification-service-using-aws-lambda-and-a-serverless-framework)
- [Github: AWS Boilerplate](https://github.com/apptension/aws-boilerplate)

## Building/Deploy my own Apps on AWS
- Sample Apps:
  + [GCP Microservices Demo App](https://github.com/GoogleCloudPlatform/microservices-demo)
  + [Weaveworks Sock Shop](https://microservices-demo.github.io/)
  + [Twitter Voting App](https://github.com/dockersamples/example-voting-app)
  + [Scaling Microservices with Message Queues, Spring Boot and Kubernetes](https://medium.com/hackernoon/scaling-microservices-with-message-queues-spring-boot-and-kubernetes-9ba4b0e48bdf)
- My App: **Stox Shop!**
  - Capabilities:
    + Allow users to create a basket of stocks. 
      - Support Symbol Look, which should make a live call and show latest information about the company
      - Support Add, Edit and Delete
      - Fields to provide: Name, Email, Stock Symbol, Number of Shares Purchased, Cost/Share, Total Cost, Date of Purchase
      - List View shows: Stock Symbol, Company Name, Number of Shares Purchased, Cost/Share, Total Cost, Date of Purchase, Total Value Now, % Gain/Loss, Status
    + Adding and/or Editing is handled using synchronous API call
    + Deleting will trigger Worker via SQS. Worker will use SNS (or SES) to send email asking for confirmation
    + User's selection of stocks as well as Audit trail is stored in Aurora Serverless (MySQL) and/or DynamoDB
    + List view is cached in ElastiCache, with Refresh functionality
  - Microservices: Web App (Fargate or EKS), Web API (Fargate or EKS, API Gateway), Worker (Lambda, API Gateway)
  - DynamoDB, ElastiCache (Redis)
  - SQS, SNS/SES

## AWS CLI Tools
- AWS CLI v2 for interacting with all your AWS resources: `aws` cli
  + [Source: AWS CLI v2 installation](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-mac.html)
  + `aws`
- AWS SAM CLI for Serverless Development: `sam`
  + `brew tap aws/tap` && `brew install aws-sam-cli`
- AWS ECS CLI 2.0 for Containers based Development: `copilot`
  + `brew install aws/tap/copilot-cli`
- Open-source tool to interact with S3: `s3cmd`
- `sls-dev-tools`
- AWS CloudFormation Linter: [`cfn-lint`](https://github.com/aws-cloudformation/cfn-python-lint)
  + `brew install cfn-lint`
- Stelligent CloudFormation Security Linter: [`cfn-nag`](https://github.com/stelligent/cfn_nag)
  + `gem install cfn-nag` OR
  + `brew install ruby brew-gem` && `brew gem install cfn-nag`