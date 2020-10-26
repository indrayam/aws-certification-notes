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
- [AWS Landing Zone](http://aws.amazon.com/answers/aws-landing-zone/) 🚧
- [AWS Compliance](https://aws.amazon.com/compliance/) 🚧
- AWS Trusted Advisor 🚧

## Part 1: Building Modern Apps in AWS
- 1. Identity & Access Management (IAM)
  + AWS Organizations 🚧
  + Users: Root Account, IAM Users, MFA, Access Key ID, Secret Access Key ✅
  + Groups ✅
  + Roles 🚧
  + Permissions via Identity and Resource Policies 🚧
- 2. Billing & Pricing
  + AWS Budgets 🚧
  + AWS Cost Explorer 🚧
  + Resource Groups 🚧
  + Tag Editor 🚧
+ Network/Security
  - 3. VPC ✅
    + 1 Region, 3 AZs ✅
    + "N" Subnets (Public/Private) ✅
    + Security Groups ✅
    + RouteTable ✅
    + Internet Gateway ✅
    + NAT Gateway
    + NACL ✅
    + VPC Endpoints
    + Elastic IP (EIP)
  - 4. Route53 ✅
  - 5. CloudFront ✅
  - 6. AWS Certificate Manager ✅
+ Compute: Virtual Machines
  - 7. EC2 ✅
    + Ubuntu 20.04 AMI ✅
    + Amazon Linux 2 AMI ✅
    + Elastic Block Store (EBS) ✅
  - 8. Elastic Load Balancing (ELB) 🚧
    - Application Load Balancing (ALB) ✅
      + Target Groups
    - Network Load Balancing (NLB) 🚧
  - 9. Auto Scaling ✅
    - Launch Configs ✅
    - Auto Scaling Groups ✅
+ Compute: PaaS, CaaS, FaaS 
  - 10. Elastic Container Service (ECS)
    - Elastic Container Registry (ECR)
  - 11. Fargate
  - 12. Elastic Kubernetes Service (EKS)
  - 13. Lambda 🚧
    - *Snowball Edge* 
  - 14. *Elastic Beanstalk*
+ Storage: Files
  - 15. Simple Secure Storage (S3) ✅
    + Athena
  - 16. *Glacier*
    - *Glacier Deep Archive*
    - *Snowball*
    - *Storage Gateway*
+ Data
  - 17. RDS 🚧
    + Aurora/MySQL
    + Aurora/Postgres
    + Postgres
    + MySQL 🚧
  - 18. DynamoDB
  - 19. ElastiCache (Redis)
  - 20. AWS ElasticSearch
  - 21. *Redshift*
+ Event-based Apps
  - 22. SQS
  - 23. SNS
  - 24. SES
  - 25. Kinesis
+ Dev**Ops**
  - 26. CloudWatch
    + Monitoring 🚧
    + Logs
    + Alarms
  - 27. CloudFormation
  - Personal Health Dashboard
+ **Dev**Ops
  - 28. CodeCommit 🚧
  - 29. CodeBuild 🚧
  - 30. CodeArtifact
  - 31. CodePipeline 🚧
  - 32. CodeDeploy 🚧

## Part 2: Diving into SecurityOps
+ Security
  - 1. CloudTrail
  = 2. AWS Config
  - 3. AWS WAF
    + AWS Firewall Manager
  - 4. AWS Shield
    + Standard
    + Advanced
  - 4. AWS Inspector
    + Extremely EC2 specific
  - 5. AWS Macie
  - 6. AWS Key Management Service (KMS)
+ Ops
  - 7. AWS X-Ray
  - 8. AWS Systems Manager
  - 9. AWS Opsworks

## Part 3: Software 2.0
1. AWS Rekognition

## Learning to build Modern Apps on AWS
- [AWS Hands-On Tutorials](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23compute%7Ccategory%23databases)
- [AWS Quick Starts](https://aws.amazon.com/quickstart/?quickstart-all.sort-by=item.additionalFields.sortDate&quickstart-all.sort-order=desc)
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
