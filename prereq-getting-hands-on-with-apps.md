# Prerequisite: Getting Hands-On with Apps

## My App: Skills
Write your own sample app using
- *Kotlin* and *Spring/SpringBoot*
- *Go*
- *MongoDB*, *Postgres*, *Redis*, *Kafka*

## My App: Starter App(s)
- Web App with a simple frontend form that submits values to a backend
- Web API that responds with a simple JSON "Hello World" payload
- Web API that integrates with *DynamoDB* (or, *MongoDB*)
- Web API that integrates with *Aurora/Postgres* (or, *PostgreSQL*)
- Web API that integrates with *ElastiCache* (or, *Redis*)
- Web API that integrates with *SNS* and/or *SQS* (or, *Kafka*)
- Lambda App that integrates with *S3*
- Lambda App that integrates with *SNS* and/or *SQS*

## My App: Getting Ops-y
- Use CloudFormation to spin up AWS infrastructure
- Use SAM to deploy Serverless Apps
- Use Code* tools to have CI/CD Pipeline
- Install Kubernetes on AWS EC2
  + Persistent Volumes
  + Nginx or Contour Ingress
  + Istio
  + Linkerd
  ...

## My App: Stox Shop! 
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

## Deploying Cloud Native Microservices Apps
- [GCP Microservices Demo App](https://github.com/GoogleCloudPlatform/microservices-demo)
- [Weaveworks Sock Shop](https://microservices-demo.github.io/)
- [Twitter Voting App](https://github.com/dockersamples/example-voting-app)
- [Scaling Microservices with Message Queues, Spring Boot and Kubernetes](https://medium.com/hackernoon/scaling-microservices-with-message-queues-spring-boot-and-kubernetes-9ba4b0e48bdf)
