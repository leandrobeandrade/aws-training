# Questões no curso Ultimate AWS Certified Cloud Practitioner

## 4º Teste (Seção 6 - EC2 Storage)

> 01] **Which EC2 Storage would you use to create a shared network file system for your EC2 Instances?**

    [ ] EBS Volume
    [ ] EC2 Instance Store
    [ ] EBS Snapshots
    [ ] EFS

> 02] **Which EC2 Storage would you use to create a shared network file system for your EC2 Instances?**

    [ ] AMI
    [ ] EC2 Image Builder
    [ ] EBS Snapshots
    [ ] IAM

> 03] **Which of the following is a fully managed native Microsoft Windows file system?**

    [ ] EFS
    [ ] FSx 
    [ ] EBS

> 04] **What are AMIs NOT used for?**

    [ ] Add your own software license
    [ ] Add your own configuration
    [ ] Add your own operating-system
    [ ] Add your own IP addresses

> 05] **EBS Volumes CANNOT be attached to multiple EC2 instances at a time.**

    [ ] True [ ] False

> 06] **An EBS Volume is a network drive you can attach to your instances while they run, so your instances' data persist even after their termination.**

    [ ] True [ ] False

> 07] **Which statement is CORRECT regarding EC2 Instance Store?**

    [ ] It is not good to use as a disk to cache content
    [ ] It has a better I/O performance, but the data is lost if the EC2 Instance is terminated
    [ ] Your data is always safe with EC2 Instance Store

> 08] **What is an EBS Snapshot?**

    [ ] The operating-system on an EC2 Instance [ ] A backup of yours EBS Volumes at a point in time
    [ ] The amount of CPU and RAM of an EC2 Instance

> 09] **Where can you find a third party's AMI so you can use it to launch your EC2 Instance?**

    [ ] Public AMIs
    [ ] My own AMIs
    [ ] AWS Marketplace AMIs

> 10] **What is an EBS Volume tied to?**

    [ ] A region
    [ ] A data center
    [ ] An edge location
    [ ] An AZ

## 5º Teste (Seção 7 - ELB/ASG)

> 01] **What is the main purpose of High Availability in the Cloud?**

    [ ] Increase scalability
    [ ] Application thriving even in case of a disaster
    [ ] Access on computers and smartphones
    [ ] Handle greater loads by launching EC2 instances based on the demand

> 02] **Which AWS offered Load Balancer should you use to handle hundreds of thousands of connections with low latency?**

    [ ] Application Load Balancer
    [ ] Network Load Balancer
    [ ] Elastic Load Balancer

> 03] **Changing an EC2 Instance Type from a t3a.medium to a t3a.2xlarge is an example of?**

    [ ] Horizontal scaling
    [ ] High Availability
    [ ] Agility
    [ ] Vertical scaling

> 04] **What can you use to handle quickly and automatically the changing load on your websites and applications by adding compute resources?**

    [ ] An Elastic Load Balancer
    [ ] A bigger instance type
    [ ] An Auto Scaling Group
    [ ] Health Checks on your instances

> 05] **Which of the following statements is INCORRECT regarding Auto Scaling Groups?**

    [ ] Replace unhealthy instances
    [ ] Are cost-effective by running at optimal capacity
    [ ] Automatically register new instances to a load balancer
    [ ] Automatically changing the EC2 instances types

> 06] **Which Load Balancer is best suited for HTTP/HTTPS load balancing traffic?**

    [ ] Network Load Balancer
    [ ] Classic Load Balancer
    [ ] Elastic Load Balancer
    [ ] Application Load Balancer

> 07] **Which of the following is NOT an Auto Scaling Strategy?**

    [ ] Manual scaling
    [ ] Dynamic scaling
    [ ] Active scaling
    [ ] Predictive scaling

> 08] **Which AWS service offers easy horizontal scaling of compute capacity?**

    [ ] EBS
    [ ] AMI
    [ ] IAM
    [ ] ASG

> 09] **Which of the following statements is NOT a feature of Load Balancers?**

    [ ] Do regular health checks to your instances
    [ ] Spread load across multiple downstream instances
    [ ] Handle failures of downstream instances
    [ ] Back-end autoscaling

## 6º Teste (Seção 8 - S3)

> 01] **Which S3 Storage Class is the most cost-effective for archiving data with no retrieval time requirement?**

    [ ] Amazon Glacier
    [ ] AWS Glacier Deep Archive
    [ ] Amazon S3 Standard-Infrequent Access
    [ ] Amazon S3 Intelligent tiering

> 02] **What hybrid AWS service is used to allow on-premises servers to seamlessly use the AWS Cloud at the storage layer?**

    [ ] Elastic Block Store
    [ ] Snowball
    [ ] S3
    [ ] Storage Gateway

> 03] **Which of the following services is a petabyte-scale data moving service (as a fleet) in or out of AWS with computing capabilities?**

    [ ] Snowcone
    [ ] Snowball Edge
    [ ] Snowmobile

> 04] **Which of the following is an exabytes-scale data moving service in or out of AWS?**

    [ ] Snowcone
    [ ] Snowball Edge
    [ ] Snowmobile

> 05] **What are Objects NOT composed of?**

    [ ] Key
    [ ] Value
    [ ] Access Keys
    [ ] Metadata

> 06] **Where are objects stored in Amazon S3?**

    [ ] Folders
    [ ] Buckets
    [ ] Files
    [ ] Bin

> 07] **A research team deployed in a location with low-internet connection would like to move 5 TBs of data to the Cloud. Which service can it use?**

    [ ] Storage Gateway
    [ ] Snowball Edge
    [ ] Snowcone
    [ ] OpsHub

> 08] **What can you use to define actions to move S3 objects between different storage classes?**

    [ ] Scaling Policy
    [ ] Bucket Policy
    [ ] Lifecycle Rules
    [ ] Replication

> 09] **A non-profit organization needs to regularly transfer petabytes of data to the cloud and to have access to local computing capacity. Which service can help with this task?**

    [ ] Snowball Edge - Storage optmized
    [ ] Snowball Edge - Compute optmized
    [ ] Snowcone
    [ ] Snowmobile

> 10] **Which S3 Storage Class is suitable for less frequently accessed data, but with rapid access when needed, while keeping a high durability and allowing an Availability Zone failure?**

    [ ] AWS S3 Standard-General Purpose
    [ ] AWS Glacier
    [ ] AWS S3 One Zone-Infrequent Access
    [ ] AWS S3 Standard-Infrequent Access

## Respostas

> 4º Teste
01) EFS
02) EC2 Image Builder
03) FSx
04) Add your own IP addresses
05) True
06) True
07) It has a better I/O performance, but the data is lost if the EC2 Instance is terminated
08) A backup of yours EBS Volumes at a point in time
09) AWS Marketplace AMIs
10) An AZ

> 5º Teste
01) Application thriving even in case of a disaster
02) NLB
03) Vertical scaling
04) Auto Scaling Group
05) Automatically changing the EC2 instances types
06) ALB
07) Active scaling
08) ASG
09) Back-end autoscaling

> 6º Teste
01) AWS Glacier Deep Archive
02) Storage Gateway
03) Snowball Edge
04) Snowmobile
05) Access Keys
06) Buckets
07) Snowcone
08) Lifecycle Rules
09) Snowball Edge - Storage optmized
10) AWS S3 Standard-Infrequent Access