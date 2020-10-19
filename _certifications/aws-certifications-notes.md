# AWS Certifications Notes

## AWS Certified Cloud Practitioner (CCP) 2020
1. AWS Global Infra: Regions, AZs
2. Core Networking: VPC, Subnets, Route Table, Security Groups, NACL, Internet Gateway, NAT Gateway, VPC Endpoints
3. Advanced Networking: Direct Connect, Hardware VPN
4. Route53
5. EC2, AMI
6. EBS
7. ELB, Classic, ALB, NLB
8. S3
9. CloudWatch, CloudWatch Logs, CloudWatch Monitoring, CloudWatch Alarms
10. Auto Scaling Groups
11. CloudFront, Distribution, Origins
12. Lambda
13. RDS, Aurora
14. DynamoDB
15. Glacier
16. Redshift
17. Elastic Beanstalk
18. CloudFormation
19. WAF (Web App Firewall)
20. Shield
21. IAM, Users, Groups, Roles, Identity Policy, Resource Policy, Organizations
22. AWS KMS, AWS CloudHSM

## Hands-On with AWS
![AWS Example Architecture v1](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v1.jpg)

![AWS Example Architecture v2](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v2.jpg)

![AWS Example Architecture v3](https://us-east-1-anand-files.s3.amazonaws.com/aws-example-architecture-v3.jpg)

- VPC
- 1 Region, 3 AZs
- "N" Subnets (Public/Private) with RouteTable, Internet Gateway, NAT Gateway, Security Groups and NACL
- Route53
- CloudFront
- AWS Certificate Manager
- S3
- ELB (ALB) tier
- EC2 running Microservices (Web App, Facade API, Data API)
  + Ubuntu 20.04 AMI
  + EBS
  + ASG
- Lambda
- RDS (Aurora)
- Glacier
- DynamoDB
- Redshift
- SQS
- CloudWatch (Monitoring, Logs, Alarms)

### Console

### CloudFormation

### Terraform

