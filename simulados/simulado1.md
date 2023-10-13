# Simulado no curso Ultimate AWS Certified Cloud Practitioner

01- **An IT company has a hybrid cloud architecture and it wants to centralize the server logs for its EC2 instances and on-premises servers. Which of the following is the MOST effective for this use-case?**

    [ ] Use AWS Lambda to send log data from EC2 instance as well as on-premises servers to CloudWatch Logs
    [ ] Use CloudWatch Logs for the EC2 instance and CloudTrail for the on-premises servers
    [ ] Use CloudTrail for the EC2 instance and CloudWatch Logs for the on-premises servers
    [ ] Use CloudWatch Logs for both the EC2 instance and the on-premises servers

02- **Which of the following S3 storage classes takes the most time to retrieve data (also known as first byte latency)?**

    [ ] S3 Intelligent-Tiering
    [ ] S3 Standard
    [ ] S3 Glacier Deep Archieve
    [ ] S3 Glacier

03- **A company's flagship application runs on a fleet of Amazon EC2 instances. As per the new policies, the system administrators are looking for the best way to provide secure shell access to AWS EC2 instances without opening new ports or using public IP addresses. Which tool/service will help you achieve this requirement?**

    [ ] AWS Inspector
    [ ] AWS System Manager Session Manager
    [ ] AWS EC2 Instance Connect
    [ ] AWS Route 53

04- **A startup runs its proprietary application on docker containers. As a Cloud Practitioner, which AWS service would you recommend so that the startup can run containers and still have access to the underlying servers?**

    [ ] AWS Lambda
    [ ] AWS Elastic Container Registry (ECR)
    [ ] AWS Fargate
    [ ] AWS Elastic Container Service (ECS)

05- **What is the primary benefit of deploying an RDS database in a Read Replica configuration?**

    [ ] Read Replica enhances database availability
    [ ] Read Replica reduces database usage costs
    [ ] Read Replica protects the database form a regional failure
    [ ] Read Replica improves database scalability

06- **What is the primary benefit of deploying an RDS database in a Multi-AZ configuration?**

    [ ] Multi-AZ reduces database usage costs
    [ ] Multi-AZ protects the database from a regional failure
    [ ] Multi-AZ enhances database availability
    [ ] Multi-AZ improves database performance for read-heavy wrokloads

07- **Multi AZ (Availability Zone) deployment is an example of which of the following?**

    [ ] High availability
    [ ] Horizontal scaling
    [ ] Vertical scaling
    [ ] Performance Efficiency

08- **A company would like to optimize Amazon EC2 costs. Which of the following actions can help with this task? (Select TWO)**

    [ ] Opt for a higher AWS Support plan
    [ ] Set up Auto Scaling Groups to align the number of instances with demand
    [ ] Vertically scale the EC2 instances
    [ ] Build its own servers
    [ ] Purchase EC2 Reserved instances

09- **Which of the following AWS Support plans provides access to online training with self-paced labs?**

    [ ] Business
    [ ] Basic
    [ ] Enterprise
    [ ] Developer

10- **A medical device company is looking for a durable and cost-effective way of storing their historic data. Due to compliance requirements, the data must be stored for 10 years. Which AWS Storage solution will you suggest?**

    [ ] AWS Storage Gateway
    [ ] S3 Glacier Deep Archieve
    [ ] S3 Glacier
    [ ] AWS EFS

11- **Which of the following is a container service of AWS?**

    [ ] AWS Fargate
    [ ] AWS SageMaker
    [ ] AWS Elastic Beanstalk
    [ ] AWS Simple Notification Service (SNS)

12- **Which of the following AWS services can be used to forecast your AWS account usage and costs?**

    [ ] AWS Budgets
    [ ] AWS Costs and Usage Reports
    [ ] AWS Pricing Calculator 
    [ ] AWs Cost Explorer

13- **An IT company wants to run a log backup process every Monday at 2 AM. The usual runtime of the process is 5 minutes. As a Cloud Practitioner, which AWS services would you recommend to build a serverless solution for this use-case? (Select two)**

    [ ] AWS CloudWatch
    [ ] AWS EC2 Instance
    [ ] AWS Lambda
    [ ] AWS System Manager
    [ ] AWS Step Function

14- **AWS Organizations provides which of the following benefits? (Select two)**

    [ ] Share the reserved EC2 instances amongst the member AWS accounts
    [ ] Check vulnerabilities on EC2 instances across the member AWS accounts
    [ ] Deploy patches on EC2 instances across the member AWS accounts
    [ ] Provision EC2 Spot instances across the member AWS accounts
    [ ] Volume discounts for Amazon EC2 and Amazon S3 aggregated across the member AWS accounts

15- **Which of the following are the best practices when using AWS Organizations? (Select TWO)**

    [ ] Restrict account privileges using Service Control Policies (SCP)
    [ ] Do not use AWS Organizations to automate AWS account creation
    [ ] Never use tags for billing
    [ ] Create accounts per department
    [ ] Disable CloudTrail on several accounts

16- **Which of the following statements is the MOST accurate when describing AWS Elastic Beanstalk?**

    [ ] It is an Infrastructure as Code which allows you to model and provision resources needed for an application
    [ ] It is a Platform as a Service (PaaS) which allows you to model and provision resources needed for an application
    [ ] It is a Platform as a Service (PaaS) which allows you to deploy and scale web applications and services
    [ ] It is an Infrastructure as a Service (IaaS) which allows you to deploy and scale web applications and services

17- **AWS Marketplace facilitates which of the following use-cases? (Select two)**

    [ ] Buy Amazon EC2 Standard Reserved Instances
    [ ] Raise request for purchasing AWS Direct Connect connection
    [ ] Purchase compliance documents from third-party vendors
    [ ] Sell Software as a Service (SaaS) solutions to AWS customers
    [ ] AWS customer can buy software that has been bundled into customized AMIs by the AWS Marketplace sellers

18- **A silicon valley based healthcare startup stores anonymized patient health data on Amazon S3. The CTO further wants to ensure that any sensitive data on S3 is discovered and identified to prevent any sensitive data leaks. As a Cloud Practitioner, which AWS service would you recommend addressing this use-case?**

    [ ] AWS Polly
    [ ] AWS Secrets Manager
    [ ] AWS Glue
    [ ] AWS Macie

19- **A Cloud Practitioner would like to get operational insights of its resources to quickly identify any issues that might impact applications using those resources. Which AWS service can help with this task?**

    [ ] AWS Personal Health Dashboard
    [ ] AWS Systems Manager
    [ ] AWS Trusted Advisor
    [ ] AWS Inspector

20- **Which policy describes prohibited uses of the web services offered by Amazon Web Services?**

    [ ] AWS Fair Use Policy
    [ ] AWS Applicable Use Policy
    [ ] AWS Acceptable Use Policy
    [ ] AWS Trusted Advisor

21- **Which AWS service can be used to subscribe to an RSS feed to be notified of the status of all AWS service interruptions?**

    [ ] AWS SNS
    [ ] AWS Lambda
    [ ] AWS Service Health Dashboard
    [ ] AWS Personal Health Dashboard

22- **Which entity ensures that your application on Amazon EC2 always has the right amount of capacity to handle the current traffic demand?**

    [ ] Multi AZ deployment
    [ ] Network Load Balancer
    [ ] Application Load Balancer
    [ ] Auto Scaling

23- **The DevOps team at an e-commerce company is trying to debug performance issues for its serverless application built using a microservices architecture. As a Cloud Practitioner, which AWS service would you recommend addressing this use-case?**

    [ ] AWS CloudFormation
    [ ] AWS X-Ray
    [ ] AWS Pinpoit
    [ ] AWS Trusted Advisor

24- **A Cloud Practitioner would like to deploy identical resources across all regions and accounts using templates while estimating costs. Which AWS service can assist with this task?**

    [ ] AWS LightSail
    [ ] AWS CodeDeploy
    [ ] AWS Directory Service
    [ ] AWS CloudFormation

25- **A photo sharing web application wants to store thumbnails of user-uploaded images on Amazon S3. The thumbnails are rarely used but need to be immediately accessible from the web application. The thumbnails can be regenerated easily if they are lost. Which is the most cost-effective way to store these thumbnails on S3?**

    [ ] Use S3 Standard to store the thumbnails
    [ ] Use S3 One-Zone Infrequent Access (One-Zone IA) to store the thumbnails
    [ ] Use S3 Standard Infrequent Access (Standard-IA) to store the thumbnails
    [ ] Use S3 Glacier to store the thumbnails

26- **Which of the following options is NOT a feature of Amazon Inspector?**

    [ ] Analyze against unintended network accessibility
    [ ] Track configuration changes
    [ ] Inspect running operating systems (OS) against known vulnerabilities
    [ ] Automate security assessments

27- **An IT company is on a cost-optimization spree and wants to identify all EC2 instances that are under-utilized. Which AWS services can be used off-the-shelf to address this use-case without needing any manual configurations? (Select two)**

    [ ] AWS Cost Explorer
    [ ] AWS Budgets
    [ ] AWS Trusted Advisor
    [ ] AWS CloudWatch
    [ ] AWS Cost and Usage Reports

28- **A data analytics company is running a proprietary batch analytics application on AWS and wants to use a storage service which would be accessed by hundreds of EC2 instances simultaneously to append data to existing files. As a Cloud Practitioner, which AWS service would you suggest for this use-case?**

    [ ] EBS
    [ ] S3
    [ ] Instance Store
    [ ] EFS

29- **Which of the following are the serverless computing services offered by AWS (Select two)**

    [ ] AWS LightSail
    [ ] AWS EC2
    [ ] AWS Elasitc Beanstalk
    [ ] AWS Lambda
    [ ] AWS Fargate

30- **An intern at an IT company provisioned a Linux based On-demand EC2 instance with per-second billing but terminated it within 30 seconds as he wanted to provision another instance type. What is the duration for which the instance would be charged?**

    [ ] 300 seconds
    [ ] 600 seconds
    [ ] 30 seconds
    [ ] 60 seconds

31- **An AWS user is trying to launch an EC2 instance in a given region. What is the region-specific constraint that the Amazon Machine Image (AMI) must meet so that it can be used for this EC2 instance?**

    [ ] An AMI is a global entity, so the region is not applicable
    [ ] You must use an AMI from the same region as that of the EC2 instance. The region of the AMI has no bearing on the performance of the EC2 instance
    [ ] You can use an AMI from a different region, but it degrades the performance of the EC2 instance
    [ ] You should use an AMI from the same region, as it improves the performance of the EC2 instance

32- **Which of the following AWS services are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)**

    [ ] AWS CloudTrail
    [ ] AWS Service Quotas
    [ ] AWS CloudFormation
    [ ] AWS Trusted Advisor
    [ ] AWS CloudWatch

33- **Which AWS Route 53 routing policy would you use to route traffic to multiple resources and also choose how much traffic is routed to each resource?**

    [ ] Weighted routing policy
    [ ] Failover routing policy
    [ ] Latency routing policy
    [ ] Simple routing policy

34- **Which pillar of the AWS Well-Architected Framework recommends maintaining infrastructure as code?**

    [ ] Security
    [ ] Performance Efficiency
    [ ] Cost Optimization
    [ ] Operational Excellence

35- **A financial services company wants to migrate from its on-premises data center to AWS Cloud. As a Cloud Practitioner, which AWS service would you recommend so that the company can compare the cost of running their IT infrastructure on-premises vs AWS Cloud?**

    [ ] AWS Pricing Calculator
    [ ] AWS Budgets
    [ ] AWS Cost Explorer
    [ ] AWS Trusted Advisor

36- **A start-up would like to quickly deploy a popular technology on AWS. As a Cloud Practitioner, which AWS tool would you use for this task?**

    [ ] AWS Quick Starts references
    [ ] AWS CodeDeploy
    [ ] AWS Forums
    [ ] AWS Whitepapers

37- **Which of the following options are the benefits of using AWS Elastic Load Balancing (ELB)? (Select TWO)**

    [ ] Less costly
    [ ] Fault tolerance
    [ ] Storage
    [ ] Agility
    [ ] High availability

38- **A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations. Which AWS technology/service will provide the necessary low-latency access to the end-users?**

    [ ] AWS Local Zones
    [ ] AWS Direct Connect
    [ ] AWS Edge Locations
    [ ] AWS Wavelength

39- **Which AWS service will you use to provision the same AWS infrastructure across multiple AWS accounts and regions?**

    [ ] AWS OpsWorks
    [ ] AWS CodeDeploy
    [ ] AWS System Manager
    [ ] AWS CloudFormation

40- **Which AWS service can be used to automate code deployment to EC2 instances as well as on-premises instances?**

    [ ] AWS CodeDeploy
    [ ] AWS CodeCommit
    [ ] AWS CloudFormation
    [ ] AWS CodePipeline

41- **Which of the following AWS authentication mechanisms supports a Multi-Factor Authentication (MFA) device that you can plug into a USB port on your computer?**

    [ ] U2F security key
    [ ] SMS text message-based MFA
    [ ] Hardware MFA device
    [ ] Virtual MFA device

42- **A financial services company wants to ensure that its AWS account activity meets the governance, compliance and auditing norms. As a Cloud Practitioner, which AWS service would you recommend for this use-case?**

    [ ] AWS CloudWatch
    [ ] AWS Config
    [ ] AWS CloudTrail
    [ ] AWS Trusted Advisor

43- **A company uses reserved EC2 instances across multiple units with each unit having its own AWS account. However, some of the units under-utilize their reserved instances while other units need more reserved instances. As a Cloud Practitioner, which of the following would you recommend as the most cost-optimal solution?**

    [ ] Use AWS Trusted Advisor to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units
    [ ] Use AWS Systems Manager to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units
    [ ] Use AWS Organizations to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units
    [ ] Use AWS Cost Explorer to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units

44- **AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)**

    [ ] AWS Lambda Functions, AWS S3
    [ ] AWS EC2 Instances, AWS EC2 Auto Scaling Groups
    [ ] AWS EFS, AWS Lambda functions
    [ ] AWS EBS volumes, AWS Lambda functions
    [ ] AWS EC2 Instances, AWS EFS

45- **Which service gives a personalized view of the status of the AWS services that are part of your Cloud architecture so that you can quickly assess the impact on your business when AWS service(s) are experiencing issues?**

    [ ] AWS Inspector
    [ ] AWS CloudWatch
    [ ] AWS Service Health Dashboard
    [ ] AWS Personal Health Dashboard

46- **Which AWS service can help you analyze your infrastructure to identify unattached or underutilized EBS volumes?**

    [ ] AWS Trusted Advisor
    [ ] AWS Inspector
    [ ] AWS Config
    [ ] AWS CloudWatch

47- **Which benefit of Cloud Computing allows AWS to offer lower pay-as-you-go prices as usage from hundreds of thousands of customers is aggregated in the cloud?**

    [ ] Go global in minutes
    [ ] Increased speed and agility
    [ ] Trade capital expense for variable expense
    [ ] Massive economies of scale

48- **A developer would like to automate operations on his on-premises environment using Chef and Puppet. Which AWS service can help with this task?**

    [ ] AWS CloudFormation
    [ ] AWS CodeDeploy
    [ ] AWS OpsWorks
    [ ] AWS Batch

49- **Which of the following AWS services offer block-level storage? (Select two)**

    [ ] EBS
    [ ] Instance Store
    [ ] ECS
    [ ] EFS
    [ ] S3

50- **A financial services enterprise plans to enable Multi-Factor Authentication (MFA) for its employees. For ease of travel, they prefer not to use any physical devices to implement MFA. Which of the below options is best suited for this use case?**

    [ ] Hardware MFA device
    [ ] U2F security key
    [ ] Soft Token MFA device
    [ ] Virtual MFA device

51- **Which of the following AWS services are always free to use (Select two)?**

    [ ] AWS S3
    [ ] AWS Auto Scaling
    [ ] AWS EC2
    [ ] AWS DynamoDB
    [ ] AWS IAM

52- **An organization deploys its IT infrastructure in a combination of its on-premises data center along with AWS Cloud. How would you categorize this deployment model?**

    [ ] Private deployment
    [ ] Hybrid deployment
    [ ] Cloud deployment
    [ ] Mixed deployment

53- **An organization maintains a separate Virtual Private Cloud (VPC) for each of its business units. Two units need to privately share data. Which is the most optimal way of privately sharing data between the two VPCs?**

    [ ] AWS Direct Connect
    [ ] VPC Peering
    [ ] VPC Endpoint
    [ ] Site-to-Site VPN

54- **A cyber-security agency uses AWS Cloud and wants to carry out security assessments on their own AWS infrastructure without any prior approval from AWS. Which of the following describes/facilitates this practice?**

    [ ] AWS Secrets Manager
    [ ] Network Stress Testing
    [ ] AWS Inspector
    [ ] Penetration Testing

55- **Which AWS service would you choose for a data processing project that needs a schemaless database?**

    [ ] AWS Aurora
    [ ] AWS RedShift
    [ ] AWS RDS
    [ ] AWS DynamoDB

56- **Which of the following are advantages of using the AWS Cloud? (Select TWO)**

    [ ] Limited scaling
    [ ] Stop guessing about capacity
    [ ] Increase speed and agility
    [ ] Trade operational expense for capital expense
    [ ] AWS is responsible for security in the cloud

57- **Due to regulatory and compliance reasons, an organization is supposed to use a hardware device for any data encryption operations in the cloud. Which AWS service can be used to meet this compliance requirement?**

    [ ] AWS Secrets Manager
    [ ] AWS Key Management Service (KMS)
    [ ] AWS CloudHSM
    [ ] AWS Trusted Advisor

58- **A company wants to improve the resiliency of its flagship application so it wants to move from its traditional database system to a managed AWS database service to support active-active configuration in both the East and West US AWS regions. The active-active configuration with cross-region support is the prime criteria for any database solution that the company considers. Which AWS database service is the right fit for this requirement?**

    [ ] AWS DynamoDB with global tables
    [ ] AWS RDS for MySQL
    [ ] AWS DynamoDB with DynamoDB Accelerator
    [ ] AWS Aurora with multi-master clusters

59- **A multi-national corporation wants to get expert professional advice on migrating to AWS and managing their applications on AWS Cloud. Which of the following entities would you recommend for this engagement?**

    [ ] Concierge Support Team
    [ ] APN Consulting Partner
    [ ] APN Technology Partner
    [ ] AWS Trusted Advisor

60- **A corporation would like to have a central user portal to log in to third-party business applications as well as accounts managed under AWS Organizations. As a Cloud Practitioner, which AWS service would you use for this task?**

    [ ] AWS CLI
    [ ] AWS IAM
    [ ] AWS Single Sign-On (SSO)
    [ ] AWS Cognito

61- **A startup wants to provision an EC2 instance for the lowest possible cost for a long-term duration but needs to make sure that the instance would never be interrupted. As a Cloud Practitioner, which of the following options would you recommend?**

    [ ] Reserved Instance
    [ ] Spot Instance
    [ ] On-Demand Instance
    [ ] Dedicated Host

62- **A unicorn startup is building an analytics application with support for a speech-based interface. The application will accept speech-based input from users and then convey results via speech. As a Cloud Practitioner, which solution would you recommend for the given use-case?**

    [ ] Use Amazon Transcribe to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech
    [ ] Use Amazon Translate to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech
    [ ] Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Translate to convey the text results via speech
    [ ] Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Transcribe to convey the text results via speech

63- **Which of the following are correct statements regarding the AWS Shared Responsibility Model? (Select two)**

    [ ] AWS is responsible for Security "of" the Cloud
    [ ] Configuration Management is the responsibility of the customer
    [ ] AWS is responsible for training AWS and customer employees on AWS products and services
    [ ] For a service like Amazon EC2, that falls under Infrastructure as a Service, AWS is responsible for maintaining guest operating system
    [ ] For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms

64- **A company would like to separate cost for AWS services by the department for cost allocation. Which of the following is the simplest way to achieve this task?**

    [ ] Create different VPCs for different departments
    [ ] Create one account for all departments and share this account
    [ ] Create tags for each department
    [ ] Create different accounts for different departments

65- **Data encryption is automatically enabled for which of the following AWS services? (Select two)?**

    [ ] AWS EBS Volumes
    [ ] AWS Redshift
    [ ] AWS S3 Glacier
    [ ] AWS Storage Gateway
    [ ] EFS drivers

## Respostas

01) Use CloudWatch Logs for both the EC2 instance and the on-premises servers
02) S3 Glacier Deep Archieve
03) AWS System Manager Session Manager
04) AWS Elastic Container Service (ECS)
05) Read Replica improves database scalability
06) Multi-AZ enhances database availability
07) High Availability
08) Set up Auto Scaling Groups to align the number of instances with demand, Purchase EC2 Reserved instances
09) Enterprise
10) S3 Glacier Deep Archieve
11) AWS Fargate
12) AWS Cost Explorer
13) CloudWatch, Lambda
14) Share the reserved EC2 instances amongst the member AWS accounts
15) Restrict account privileges using Service Control Policies (SCP), Create accounts per department
16) It is a Platform as a Service (PaaS) which allows you to deploy and scale web applications and services
17) Sell Software as a Service (SaaS) solutions to AWS customers, AWS customer can buy software that has been bundled into customized AMIs by the AWS Marketplace sellers
18) AWS Macie
19) AWS Systems Manager
20) AWS Acceptable Use Policy
21) AWS Service Health Dashboard
22) Auto Scaling
23) AWS X-Ray
24) AWS CloudFormation
25) Use S3 One-Zone Infrequent Access (One-Zone IA) to store the thumbnails
26) Track configuration changes
27) AWS Cost Explorer, AWS Trusted Advisor
28) EFS
29) AWS Lambda, AWS Fargate
30) 60 seconds
31) You must use an AMI from the same region as that of the EC2 instance. The region of the AMI has no bearing on the performance of the EC2 instance
32) AWS Service Quotas, AWS Trusted Advisor
33) Weighted routing policy
34) Operational Excellence
35) AWS Pricing Calculator
36) AWS Quick Starts references
37) Fault tolerance, High availability
38) AWS Local Zones
39) AWS CloudFormation
40) AWS CodeDeploy
41) U2F security key
42) CloudTrail
43) Use AWS Organizations to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units
44) AWS EC2 Instances, AWS EC2 Auto Scaling Groups, AWS EBS volumes, AWS Lambda functions
45) AWS Personal Health Dashboard
46) AWS Trusted Advisor
47) Massive economies of scale
48) AWS OpsWorks
49) EBS, Instance Store
50) Virtual MFA device
51) AWS Auto Scaling, DynamoDB
52) Hybrid deployment
53) VPC Peering
54) Penetration Testing
55) AWS DynamoDB
56) Stop guessing about capacity, Increase speed and agility
57) AWS CloudHSM
58) AWS DynamoDB with global tables
59) APN Consulting Partner
60) AWS Single Sign-On (SSO)
61) Reserved Instance
62) Use Amazon Transcribe to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech
63) AWS is responsible for Security "of" the Cloud, For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms
64) Create tags for each department
65) AWS S3 Glacier, AWS Storage Gateway