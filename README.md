# AWS Nerd Notes

## AWS App Architecture Samples
![AWS Example Architecture v1](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v1.jpg)

![AWS Example Architecture v2](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v2.jpg)

![AWS Example Architecture v3](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v3.jpg)

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

## Part 0: Best-Practice/Cost Optimization Enablers
- [AWS Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html) 🚧
- [AWS Pricing Calculator](https://calculator.aws/#/) 🚧
- [AWS Architecture Center](https://aws.amazon.com/architecture/?awsf.quickstart-architecture-page-filter=highlight%23new) 🚧
  + [AWS Well Architected](https://aws.amazon.com/architecture/well-architected/?achp_wa1&wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)
- [AWS Quick Starts](https://aws.amazon.com/quickstart/?quickstart-all.sort-by=item.additionalFields.sortDate&quickstart-all.sort-order=desc) 🚧
- [AWS Compliance](https://aws.amazon.com/compliance/) 🚧
- AWS Trusted Advisor 🚧
- AWS Well Architected Tool

## Part 1: Building Modern Apps in AWS
- 1. AWS Identity & Access Management (IAM)
  + AWS Organizations 🚧
  + Users: Root Account, IAM Users, MFA, Access Key ID, Secret Access Key ✅
  + Groups ✅
  + Roles 🚧
  + Permissions via Identity and Resource Policies 🚧
  + 2. AWS Control Tower
    - [AWS Landing Zone](http://aws.amazon.com/answers/aws-landing-zone/)
  + 3. *Amazon Cloud Directory*
  + 4. *Amazon Directory Service*
  + 5. *AWS Single Sign-On*
- 6. Billing Dashboard for Cost Management
  + AWS Budgets 🚧
  + AWS Cost Explorer 🚧
  + AWS Cost and Usage Reports
  + Reserved Instance Reporting
  + Tag Editor 🚧
+ Network/Security
  - 7. VPC ✅
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
  - 8. Route53 ✅
  - 9. CloudFront ✅
  - 10. Amazon API Gateway
  - 11. AWS App Mesh
  - 12. AWS Cloud Map
  - 13. *AWS Transit Gateway* (think, Cisco SCI) 🚧
  - 14. *AWS Direct Connect*
  - 15. *AWS Global Accelerator*
+ Compute: Virtual Machines
  - 16. EC2 ✅
    + Ubuntu 20.04 AMI ✅
    + Amazon Linux 2 AMI ✅
    + Elastic Block Store (EBS) ✅
    + Auto Scaling ✅
      - Launch Configs ✅
      - Auto Scaling Groups ✅
  - 17. Elastic Load Balancing (ELB) 🚧
    + Application Load Balancing (ALB) ✅
      - Target Groups
    + Network Load Balancing (NLB) 🚧
+ Compute: PaaS, CaaS, FaaS 
  - 18. AWS Elastic Container Service (ECS)
    + 19. AWS Elastic Container Registry (ECR)
  - 20. AWS Fargate
  - 21. AWS Elastic Kubernetes Service (EKS)
  - 22. AWS Lambda 🚧
  - 23. *AWS Elastic Beanstalk*
  - 24. *Amazon Lightsail* (v. DigitalOcean)
  - 25. AWS Batch
+ Storage: Files
  - 26. Amazon Simple Secure Storage (S3) ✅
  - 27. Amazon Elastic File System
  - 28. *Amazon S3 Glacier & S3 Glacier Deep Archive*
  - 29. AWS Storage Gateway (Hybrid storage service that enables your on-premises apps to seamlessly use AWS cloud storage)
+ Data
  - 30. RDS 🚧
    + Aurora/MySQL
    + Aurora/Postgres
    + Postgres
    + MySQL 🚧
  - 31. Amazon DynamoDB
  - 32. Amazon ElastiCache (Redis)
  - 33. *Amazon Neptune*
  - 34. *Amazon Quantum Ledger Database (QLDB)*
  - 35. *Amazon Timestream*
  - 36. *Amazon DocumentDB (MongoDB compatibility)*
+ Event-based Apps
  - 37. Amazon Simple Notification Service (SNS)
  - 38. Amazon Simple Queue Service (SQS)
    + 39. Amazon MQ (Managed Apache ActiveMQ service)
  - 40. AWS Step Functions (Workflow Engine, vs. Airflow, Argo)
    + 41. AWS Simple Workflow Service (SWF)
+ Dev**Ops**
  - 42. Amazon CloudWatch
    + Monitoring 🚧
    + Logs
    + Alarms
  - 43. AWS Systems Manager
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
  - 44. AWS X-Ray
  - 45. AWS Auto Scaling
  - 46. CloudFormation
  - 47. CloudTrail
  - 48. AWS Config
  - 49. *AWS Opsworks*
    + Chef
    + Puppet 
  - 50. AWS Service Catalog
  - 51. Personal Health Dashboard
  - 52. AWS License Manager
+ **Dev**Ops
  - 53. CodeCommit 🚧
  - 54. CodeBuild 🚧
  - 55. CodeArtifact
  - 56. CodePipeline 🚧
  - 57. CodeDeploy 🚧

## Part 2: Security
Security
  - 1. AWS Security Hub
  - 2. AWS Certificate Manager ✅
  - 3. AWS WAF
    + AWS Firewall Manager
  - 4. AWS Shield
    + Standard
    + Advanced
  - 5. AWS Inspector
    + Extremely EC2 specific
  - 6. Amazon GuardDuty
  - 7. AWS Macie
  - 8. AWS Secrets Manager (v. Vault)
  - 9. AWS Key Management Service (KMS)
  - 10. AWS CloudHSM (Hardware Security Module)
  - 11. AWS Artifact

## Part 4: Big Data & BI Analytics
- 1. *Amazon Athena* (SQL on S3)
- 2. *Amazon EMR* (Managed Hadoop Framework)
  + Hadoop
  + Spark
  + HBase
  + Presto
  + Flink
- 3. *Amazon CloudSearch*
- 4. Amazon Elasticsearch
- 5. Amazon Kinesis (Distributed Commit log for Streaming/Processing Data; vs. Kafka/Kafka Streams/kSQL)
  + Kinesis Data Firehose
  + Kinesis Data Streams
  + Kinesis Data Analytics
  + *Kinesis Video Streams*
  + Amazon Managed Streaming for Kafka (MSK)
- 6. *Amazon Redshift (Data Warehouse; vs. BigQuery or Snowflake)*
- 7. *Amazon QuickSight* (Business Intelligence Service; vs. Tableau, Microsoft Power BI)
- 8. *AWS Glue* (Managed Extract Transform and Load (ETL) Service, vs. Informatica)
- 9. *AWS Data Pipeline* (Movement and Transformation of data)
- 10. *AWS Lake Formation* (Data Lakes, vs. Snowflake)

## Part 3: Software 2.0

### Artifical Intelligence
1. AWS SageMaker
  + AWS SageMaker Ground Truth
2. Amazon Comprehend (NLP service that uses machine learning to find insights and relationships in text)
3. Amazon Lex (Build conversational interfaces into any app using voice and text. Speech recognition and natural language understanding are some of the most challenging problems to solve in computer science. Lex brings Alexa's tech!)
4. Amazon Polly (Service that turns text into lifelike speech! Lets you create apps that talk!!)
5. Amazon Rekognition (Service that makes it easy to add image analysis to apps)
6. Amazon Translate (Machine Translation service that delivers fast, high-quality, and affordable language translation)
7. Amazon Transcribe (Automatic Speech Recognition (ASR) service. Makes it easy for developers to speech-to-text capability to apps)
8. Amazon Textract (Service that automatically extracts data from scanned docs. Goes beyond OCR to read data from form fields and tables)
9. Amazon Forecast (Service that uses machine learning to deliver high quality accurate business forecasts)
10. Amazon Personalize (Service that uses machine learning to help apps create individualized recommendations for their users/customers) 
11. Amazon Deep Learning AMIs (Helps ML practitioners by giving them infra/tools to accelerate deep learning in the cloud)
12. AWS DeepLens (Helps developers get started with Deep Learning)
13. AWS DeepRacer (Helps developers get started with reinforcement learning(RL))
14. Apache MXNet on AWS
15. TensorFlow on AWS
16. Amazon Elastic Inference (Allows you to attach low-cost GPU-powered acceleration to Amazon EC2 and SageMaker instances to reduce cost of running deep learning inference)
17. AWS Inferentia (Machine Learning inference chip designed to deliver high performance at low cost. Making predictions using a trained machine learning model - a process called "inference" - can drive as much as 90% of the compute costs of the app. While Amazon Elastic Inference can reduce costs by up to 75%, some inference workloads require an entire GPU or have extremely low latency requirements. Solving this at low cost requires a dedicated inference chip!) 

### Robotics
1. AWS Robomaker (Service that makes it easy to develop, test and deploy intelligent robotics apps)

### Satellite
1. AWS Ground Station (Fully managed service that lets you control satellite communications, downlink and process satellite data etc.)

## AWS Online Learning Materials
- [AWS Architecture Center](https://aws.amazon.com/architecture/?icmpid=link_from_docs_website)
- [AWS Archirecture Monthly](https://aws.amazon.com/whitepapers/kindle/?icmpid=link_from_docs_website)
- [AWS Hands-On Tutorials](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23compute%7Ccategory%23databases)
- [AWS Quick Starts](https://aws.amazon.com/quickstart/?quickstart-all.sort-by=item.additionalFields.sortDate&quickstart-all.sort-order=desc)
- [AWS Free Digital Training](https://www.aws.training/LearningLibrary?filters=language%3A1&filters=digital%3A1&tab=view_all)
- [AWS Workshops](https://awsworkshop.io/)
  + [AWS Security Workshops](https://awssecworkshops.com/)
  + [AWS Global Accelerator Workshop](https://intro-to-global-accelerator.workshop.aws/)
- [AWS Whitepapers & Guides](https://aws.amazon.com/whitepapers/?icmpid=link_from_docs_website&whitepapers-main.sort-by=item.additionalFields.sortDate&whitepapers-main.sort-order=desc)

## Building Apps on AWS
- Deploy Sample Modern Apps on AWS:
  + [GCP Microservices Demo App](https://github.com/GoogleCloudPlatform/microservices-demo)
  + [Weaveworks Sock Shop](https://microservices-demo.github.io/)
  + [Twitter Voting App](https://github.com/dockersamples/example-voting-app)
  + [Scaling Microservices with Message Queues, Spring Boot and Kubernetes](https://medium.com/hackernoon/scaling-microservices-with-message-queues-spring-boot-and-kubernetes-9ba4b0e48bdf)
  + My App (Stocks Rock!):
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
