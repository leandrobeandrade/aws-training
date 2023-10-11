# Questões no curso Ultimate AWS Certified Cloud Practitioner

## 9º Teste (Seção 11 - Deployments & Managing Infrastructure at Scale)

> 01] **CodeStar can be used to monitor and check the health of an environment.**

    [ ] True [ ] False

> 02] **Which AWS managed service allows to automate software deployments to a hybrid mix of EC2 Instances and On-Premises servers?**

    [ ] CodeDeploy
    [ ] CloudFormation
    [ ] Elastic Beanstalk
    [ ] CodeStar
    
> 03] **You are a software developer working on a project with your team. You need a secure and reliable version control system to store, share, and collaborate your code with the team. Which AWS service can help the developers?**

    [ ] CodeDeploy
    [ ] CodeCommit
    [ ] CodePipeline
    [ ] Cloud9

> 04] **You need a unified user interface that gives you visibility, control, and patching capabilities for your EC2 Instances on AWS, as well as for servers running in your on-premises data centers. Which service should you use?**

    [ ] Storage Gateway
    [ ] OpsWorks
    [ ] Elastic Container Service (ECS)
    [ ] System Manager (SSM)

> 05] **You need to use Chef or Puppet. Which AWS service should you use?**

    [ ] CloudFormation
    [ ] CodeDeploy
    [ ] OpsWorks
    [ ] CodeCommit

> 06] **A developer would like to deploy infrastructure on AWS but only knows Python. Which AWS service can assist him?**

    [ ] SDK - Sofware Development Kit
    [ ] CDK - Cloud Development Kit
    [ ] CloudFormation
    [ ] CodeBuild

> 07] **Which of the following allows you to deploy any AWS Infrastructure as a Code?**

    [ ] Elastic Beanstalk
    [ ] OpsWorks
    [ ] CloudFormation
    [ ] System Manager (SSM)

> 08] **A new startup would like an online integrated development environment (IDE) to write, run, and debug code. Which AWS service can help with this task?**

    [ ] Cloud9
    [ ] OpsWorks
    [ ] CodeArtifact
    [ ] CodeStar

> 09] **Which service is referred to as a Platform as a Service (PaaS)?**

    [ ] Elastic Beanstalk
    [ ] OpsWorks
    [ ] CloudFormation
    [ ] EC2

> 10] **What is called the declaration of the AWS resources that make up a stack?**

    [ ] CloudFormation Schemas
    [ ] CloudFormation Diagrams
    [ ] CloudFormation Templates
    [ ] CloudFormation Models

> 11] **Which of the following services can a developer use to store code dependencies?**

    [ ] CodeBuild
    [ ] CodeCommit
    [ ] Cloud9
    [ ] CodeArtifact

> 12] **CodeStar can orchestrate the different steps to have code automatically pushed to production, while CodePipeline is a unified UI to easily manage software development activities in one place.**

    [ ] True [ ] False

> 13] **Which serverless service can be used to build code and run tests?**

    [ ] CodeStar
    [ ] CDK - Cloud Development Kit
    [ ] CodePipeline
    [ ] CodeBuild

> 14] **CloudFormation and Elastic Beanstalk are free of use.**

    [ ] True [ ] False 

## 10º Teste (Seção 12 - Global Infrastructure)

> 01] **Which Route 53 Routing Policies would you use to route traffic to multiple resources in proportions that you specify?**

    [ ] Simple Routing Policy
    [ ] Weighted Routing Policy (Ponderado)
    [ ] Latency Routing Policy
    [ ] Failover Routing Policy

> 02] **Which service is optimized to deploy ultra-low latency applications to 5G devices?**

    [ ] WaveLength
    [ ] Route53
    [ ] CloudFront

> 03] **You need to enable fast, easy, and secure transfers of files over long distances on S3. Which service would you use?**

    [ ] AWS Global Accelerator
    [ ] S3 Transfer Acceleration 
    [ ] S3 Cross-Region Replication

> 04] **What does AWS CloudFront use to improve read performance?**

    [ ] DDoS Protection
    [ ] S3 Buckets Fast-Read
    [ ] Caching Content in Edge Locations
    [ ] Caching Content in Edge Regions

> 05] **Which service can be used to run AWS infrastructure and services on-premises for a hybrid cloud architecture?**

    [ ] CloudFront
    [ ] Outposts
    [ ] DMS
    [ ] Storage Gateway

> 06] **Which of the following statements is NOT a reason for a global application?**

    [ ] Decreased Latency
    [ ] Disaster Recovery
    [ ] Scale elastically on demand
    [ ] Attack protection

> 07] **Which features are available with Route 53?**

    [ ] Health Checks, Auto Scalling, Routing Policy, DNS
    [ ] Load Balancing, DNS, Domain Registration, Monitoring
    [ ] Domain Registration, DNS, Health Checks, DDoS Protection
    [ ] Domain Registration, DNS, Health Checks, Routing Policy

> 08] **With which services does CloudFront integrate to protect against web attacks?**

    [ ] WAF & Shield
    [ ] WAF & IAM
    [ ] IAM & Shield
    [ ] Security Groups & WAF

## 11º Teste (Seção 13 - Cloud Integrations)

> 01] **A company using Apache ActiveMQ is migrating to the cloud. Which AWS service can it use to easily set up and operate its message brokers in the cloud?**

    [ ] AWS Simple Queue Service (SQS)
    [ ] AWS Simple Notification Service (SNS)
    [ ] AWS MQ
    [ ] AWS Kinesis

> 02] **Which service is a fully managed pub/sub messaging service that makes it easy to set up, operate, and send notifications from the cloud, using a push-based system?**

    [ ] AWS Simple Notification Service (SNS)
    [ ] AWS Simple Queue Service (SQS)
    [ ] Auto Scalling Groups (ASG)

> 03] **You can use Kinesis to perform real-time analysis from video streams.**

    [ ] True [ ] False

> 04] **Which principle is mainly applied when using Amazon SQS or Amazon SNS?**

    [ ] Scalability
    [ ] Automation
    [ ] Decouple your applications

> 05] **Which service allows you to send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available, using a pull-based system?**

    [ ] AWS Simple Notification Service (SNS)
    [ ] AWS Simple Queue Service (SQS)
    [ ] Auto Scalling Groups (ASG)

## Respostas

> 9º Teste
01) False
02) CodeDeploy
03) CodeCommit
04) SSM - System Manager
05) OpsWorks
06) CDK - Cloud Development Kit
07) CloudFormation
08) Cloud9
09) Elastic Beanstalk
10) CloudFormation Templates
11) CodeArtifact
12) False (as funcionalidades são ao contrário)
13) CodeBuild
14) True

> 10º Teste
01) Weighted Routing Policy (Ponderado)
02) WaveLenght
03) S3 Transfer Acceleration
04) Caching Content in Edge Locations
05) Outposts
06) Scale elastically on demand
07) Domain Registration, DNS, Health Checks, Routing Policy
08) WAF & Shield

> 11º Teste
01) AWS MQ
02) AWS Simple Notification Service (SNS)
03) True
04) Decouple your applications
05) AWS Simple Queue Service (SQS)