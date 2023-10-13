# Questões no curso Ultimate AWS Certified Cloud Practitioner

## 12º Teste (Seção 14 - Cloud Monitoring)

> 01] **Which CloudWatch feature would you use to trigger notifications when a metric reaches a threshold you specify?**

    [ ] CloudWatch Events
    [ ] CloudWatch Logs
    [ ] CloudWatch Alarms
    [ ] CloudWatch Triggers

> 02] **Which AWS service helps developers analyze and debug production as well as distributed applications?**

    [ ] CloudWatch
    [ ] X-Ray
    [ ] Service Health Dashboard
    [ ] CloudTrail

> 03] **Which AWS service provides alerts and remediation guidance when AWS is experiencing events that may impact you?**

    [ ] Service Health Dashboard
    [ ] CloudWatch
    [ ] AWS Health Dashboard
    [ ] CloudTrail

> 04] **You need to set up metrics monitoring for every service in AWS. Which service would you use?**

    [ ] CloudTrail
    [ ] X-Ray
    [ ] CloudWatch
    [ ] Service Health Dashboard

> 05] **Which service allows you to inspect, audit, and record events and API calls made within your AWS account?**

    [ ] X-Ray
    [ ] CloudWatch
    [ ] CloudTrail

> 06] **Which AWS service automatically analyzes code and provides performance recommendations?**

    [ ] X-Ray
    [ ] CodePipeline
    [ ] CodeGuru

> 07] **How would you describe Amazon CloudWatch Logs?**

    [ ] A single, highly scalabe service that centralizes the logs from all of your systems, applications, and AWS services that you use
    [ ] A service that provides a real-time stream of system events that describe changes in AWS resources
    [ ] A service that enables governance, compliance, operational auditing, and risk auditing of your AWS account 
    [ ] A service that lets you run code without provisioning or managing servers

> 08] **If a resource is deleted in AWS, which service should you use to investigate first?**

    [ ] CloudTrail
    [ ] CloudWatch Logs
    [ ] Personal Health Dashboard

## 13º Teste (Seção 15 - VPC & Network)

> 01] **Your private subnets need to connect to the Internet while still remaining private. Which AWS-managed VPC component allows you to do this?**

    [ ] NAT Instances
    [ ] Internet Gateway
    [ ] Security Groups
    [ ] NAT Gateways

> 02] **A public subnet is accessible from the Internet while a private subnet is not accessible from the Internet.**

    [ ] Yes
    [ ] No, all subnets are accessible from the internet
    [ ] No, all subnets are not accessible from the internet

> 03] **Which type of firewall has both ALLOW and DENY rules and operates at the subnet level?**

    [ ] NACL (Network Access Control List)
    [ ] Web Application Firewall (WAF)
    [ ] Security Groups
    [ ] GuardDuty

> 04] **You would like to connect hundreds of VPCs and your on-premises data centers together. Which AWS service allows you to do link all these together efficiently?**

    [ ] Site-to-Site VPN
    [ ] Transit Gateway
    [ ] Internet Gateway
    [ ] AWS Direct Connect

> 05] **A company needs two VPCs to communicate with each other. What can they use?**

    [ ] VPC Endpoints
    [ ] Direct Conect
    [ ] Internet Gateway
    [ ] VPC Peering

> 06] **You need a logically isolated section of AWS, where you can launch AWS resources in a private network that you define. What should you use?**

    [ ] Subnets
    [ ] AZ's
    [ ] A VPC
    [ ] NAT Instances

> 07] **A company needs to have a private, secure, and fast connection between its on-premises data centers and the AWS Cloud. Which connection should they use?**

    [ ] AWS Conect
    [ ] Site-to-Site VPN
    [ ] VPC Peering
    [ ] AWS Direct Connect

> 08] **Your VPC needs to connect with the Internet. Which VPC component can help?**

    [ ] NAT Gateways
    [ ] NAT Instances
    [ ] NACL (Network Access Control List)
    [ ] Internet Gateway

## 14º Teste (Seção 16 - Security & Compliance)

> 01] **Data sitting on an RDS instance would be referred to as?**

    [ ] Data in transit
    [ ] Data at rest (Dados em repouso)
    [ ] Encrypted data

> 02] **According to the Shared Responsibility Model, who is responsible for firewall and network configuration for EC2 Instances?**

    [ ] AWS
    [ ] Customer
    [ ] AWS and customer

> 03] **Which of the following services can you use to discover and protect your sensitive data in AWS?**

    [ ] Macie
    [ ] Shield
    [ ] Artifact
    [ ] X-Ray

> 04] **Which AWS service lets you quickly find the root of potential security issues to take faster actions?**

    [ ] Inspector
    [ ] Detective
    [ ] CloudWatch
    [ ] WAF - Web Application Firewall

> 05] **A company would like to protect its web applications from common web exploits that may affect availability, compromise security, or consume excessive resources. Which AWS service should they use?**

    [ ] Auto Scaling Groups (ASG)
    [ ] Shield
    [ ] CloudHSM
    [ ] WAF - Web Application Firewall

> 06] **Where can you find on-demand access to AWS compliance documentation and AWS agreements?**

    [ ] Artifact
    [ ] Personal Health Dashboard
    [ ] Secrets Manager
    [ ] Shared Responsibility Model

> 07] **You can perform any kind of penetration testing on any AWS service without prior approval.**

    [ ] True [ ] False

> 08] **You want to record configurations and changes over time. Which service allows you to do this?**

    [ ] Config
    [ ] Inspector
    [ ] GuardDuty
    [ ] Secrets Manager

> 09] **A company would like to secure network communications using SSL & TLS certificates. Which AWS service can it use?**

    [ ] ACM - AWS Certificate Manager
    [ ] Secrets Manager
    [ ] Macie
    [ ] WAF - Web Application Firewall

> 10] **According to the Shared Responsibility Model, who is responsible for Patch Management?**

    [ ] AWS
    [ ] Customer
    [ ] AWS & Customer

> 11] **You want to centrally automate security checks across several AWS accounts. Which AWS service can you use?**

    [ ] Macie
    [ ] Detective
    [ ] CloudTrail
    [ ] Secutiry Hub

> 12] **Which of the following services is managed by AWS and is used to manage encryption keys?**

    [ ] CloudHSM
    [ ] KMS - Key Management Service
    [ ] Secrets Manager
    [ ] IAM

> 13] **A company would like to automate security on EC2 instances to assess security and vulnerabilities in these instances. Which AWS service should it use?**

    [ ] Config
    [ ] Trusted Advisor
    [ ] Inspector
    [ ] Systems Manager

> 14] **Which of the following actions does NOT require the root user?**

    [ ] Close your AWS account
    [ ] Change your AWS Support plan
    [ ] Register as a seller in the Reserved Instance Marketplace 
    [ ] Access the billing dashboard

> 15] **According to the Shared Responsibility Model, who is responsible for protecting hardware?**

    [ ] AWS
    [ ] Customer
    [ ] AWS & Customer

> 16] **Which AWS service's ONLY role is to safeguard running applications from DDoS attacks?**

    [ ] WAF - Web Application Firewall
    [ ] Shield
    [ ] CloudFront
    [ ] KMS - Key Management Service

> 17] **Which service is a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts and workloads?**

    [ ] KMS - Key Management Service
    [ ] WAF - Web Application Firewall
    [ ] Inspector
    [ ] GuardDuty

> 18] **Which of the following options is NOT a situation where you should contact the AWS Abuse team?**

    [ ] DDoS attack from AWS-owned IP addresses
    [ ] Spam from AWS-owned IP addresses or AWS resources
    [ ] Hosting objectionable or copyrighted content on AWS
    [ ] Losing MFA Device

## Respostas

> 12º Teste
01) CloudWatch Alarm
02) X-Ray
03) AWS Health Dashboard
04) CloudWatch
05) CloudTrail
06) CodeGuru
07) A single, highly scalabe service that centralizes the logs from all of your systems, applications, and AWS services that you use
08) CloudTrail

> 13º Teste
01) NAT Gateways
02) Yes
03) NACL (Network Access Control List)
04) Transit Gateway
05) VPC Peering
06) VPC
07) Direct Connect
08) Internet Gateway

> 14º Teste
01) Data at rest (Dados em repouso)
02) Customer
03) Macie
04) Detective
05) WAF - Web Application Firewall
06) Artifact
07) False
08) Config
09) ACM - AWS Certificate Manager
10) AWS & Customer
11) Secutiry Hub
12) KMS - Key Management Service
13) Inspector
14) Access the billing dashboard
15) AWS
16) Shield
17) GuardDuty
18) Losing MFA Device