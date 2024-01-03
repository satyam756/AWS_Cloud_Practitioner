# AWS_Cloud_Practitioner
> Notes for AWS Cloud Practitioner

- [Introduction](#introduction)
  - [Private cloud - rockspace](#private-cloud---rockspace)
  - [public cloude - Azure, Google Cloud, AWS](#public-cloude---azure-google-cloud-aws)
  - [Hybrid cloude - mix of both private and public cloud](#hybrid-cloude---mix-of-both-private-and-public-cloud)
- [Characterstics of cloud computing](#characterstics-of-cloud-computing)
- [Advantages of cloud computing](#advantages-of-cloud-computing)
- [problems solved by cloud](#problems-solved-by-cloud)
- [Types of Cloud Computing](#types-of-cloud-computing)
- [Pricing of the cloud](#pricing-of-the-cloud)
- [AWS Cloud History](#aws-cloud-history)
- [Identity Access Management (IAM)](#identity-access-management-iam)
- [IAM Best Practices](#iam-best-practices)
- [Amazon EC2](#amazon-ec2)
- [EC2 sizing and configucation options:](#ec2-sizing-and-configucation-options)
- [creating a Instance running linux](#creating-a-instance-running-linux)
- [use this for your user data (script from top to bottom)](#use-this-for-your-user-data-script-from-top-to-bottom)
- [install httpd (linux 2 version)](#install-httpd-linux-2-version)
- [Security Groups:](#security-groups)
- [SSH Troubleshooting](#ssh-troubleshooting)
- [do not add IAM credentials or the secret key](#do-not-add-iam-credentials-or-the-secret-key)
- [EBS (Elastic Block store)](#ebs-elastic-block-store)
- [About EBS Multi-Attach](#about-ebs-multi-attach)
- [Amazon Machine Image](#amazon-machine-image)
- [EFS - Elastic File System](#efs---elastic-file-system)
- [Vertical Scalablity:](#vertical-scalablity)
- [Horizontal Scalablity:](#horizontal-scalablity)
- [High availablity:](#high-availablity)
- [Scalablity vs Elasticity (vs Agility)](#scalablity-vs-elasticity-vs-agility)
  - [what is load balancing:](#what-is-load-balancing)
- [why use a load balancers:](#why-use-a-load-balancers)
- [ALB (Application load balancers):](#alb-application-load-balancers)
- [NLB (Network load balancers):](#nlb-network-load-balancers)
- [GLB (Gateway load balancers):](#glb-gateway-load-balancers)
- [Auto Scaling Group:](#auto-scaling-group)
- [Scaling Strategies](#scaling-strategies)
- [Amazon S3 uses Cases](#amazon-s3-uses-cases)
  - [Amazon S3 Buckets:](#amazon-s3-buckets)
  - [Amazon S3 - objects (cont):](#amazon-s3---objects-cont)
  - [Use S3 Bucket for policy to:](#use-s3-bucket-for-policy-to)
- [use Policy generator to create a json file](#use-policy-generator-to-create-a-json-file)
- [AWS Snow Family](#aws-snow-family)
  - [AWS SnowCone and SnowCone SSD](#aws-snowcone-and-snowcone-ssd)
  - [AWS Snowmobile](#aws-snowmobile)
- [AWS Snow Family for Data Migration](#aws-snow-family-for-data-migration)
- [Snow Family - Usage process](#snow-family---usage-process)
- [for SnowBall Edge computing](#for-snowball-edge-computing)
- [AWS OpsHub](#aws-opshub)
- [Snowball edge pricing](#snowball-edge-pricing)
- [AWS Storage Gateway](#aws-storage-gateway)
- [AWS Storage Cloud Native Options:](#aws-storage-cloud-native-options)
  - [Types of Storage gateways:](#types-of-storage-gateways)
- [AWS RDS](#aws-rds)
  - [Advantages over RDS vs deploying DB on EC2:](#advantages-over-rds-vs-deploying-db-on-ec2)
- [Amazon Aurora](#amazon-aurora)
- [Amazon Aurora Serverless](#amazon-aurora-serverless)
- [Amazon ElastiCache Overview:](#amazon-elasticache-overview)
- [Dynamo DB](#dynamo-db)
  - [DynamoDB Accelerator - DAX](#dynamodb-accelerator---dax)
- [Redshift database](#redshift-database)
- [Redshift Serverless](#redshift-serverless)
- [Amazon EMR (Elastic MapReduce):](#amazon-emr-elastic-mapreduce)
- [Amazon Athena:](#amazon-athena)
- [Amazon QuickSight](#amazon-quicksight)
- [DocumentDB:](#documentdb)
- [Amazon Neptune:](#amazon-neptune)
- [Amazon QLDB (Quantum ledger Database)](#amazon-qldb-quantum-ledger-database)
- [Amazon Managed Blockchain:](#amazon-managed-blockchain)
- [AWS Glue:](#aws-glue)
- [DMS - Database Migration Service](#dms---database-migration-service)
- [Docker](#docker)
- [ECS - Elastic Container Service:](#ecs---elastic-container-service)
- [Fargate](#fargate)
- [ECR - Elastic Contianer Registry](#ecr---elastic-contianer-registry)
- [Lambda:](#lambda)
  - [AWS Lambda lanugage support](#aws-lambda-lanugage-support)
  - [AWS Lambda Pricing:](#aws-lambda-pricing)
- [Amazon API Gateway:](#amazon-api-gateway)
- [AWS Batch:](#aws-batch)
- [Batch vs Lambda:](#batch-vs-lambda)
- [Amazon Lightsail:](#amazon-lightsail)
- [AWS Cloud Development Kit (CDK):](#aws-cloud-development-kit-cdk)
- [3 Architecture models of Elastic BeanStalk:](#3-architecture-models-of-elastic-beanstalk)
- [Elastic Beanstalk supports platforms](#elastic-beanstalk-supports-platforms)
  - [Elastic Beanstalk - Health Monitoring](#elastic-beanstalk---health-monitoring)
- [AWS CodeDeploy](#aws-codedeploy)
- [Code Commit](#code-commit)
- [Code Build:](#code-build)
- [AWS CodePipeline:](#aws-codepipeline)
- [AWS CodeArtifacts](#aws-codeartifacts)
- [AWS CodeStar](#aws-codestar)
- [AWS Cloud9](#aws-cloud9)
- [AWS System Manager (SSM)](#aws-system-manager-ssm)
  - [How System Manager works(SSM)](#how-system-manager-worksssm)
  - [SSM Session Manager (System Manager)](#ssm-session-manager-system-manager)
  - [Systems Manager Parameter Store (SSM)](#systems-manager-parameter-store-ssm)
- [AWS OpsWorks](#aws-opsworks)
- [Deployment Summary:](#deployment-summary)
- [Developer Services Summary:](#developer-services-summary)
- [AWS Global application](#aws-global-application)
  - [Why make a Global Application?](#why-make-a-global-application)
- [Global AWS Infrastructure](#global-aws-infrastructure)
  - [Global applications in AWS](#global-applications-in-aws)
- [Amazon Route 53](#amazon-route-53)
  - [Route 53 Routing policies](#route-53-routing-policies)
- [AWS CloudFront](#aws-cloudfront)
  - [CloudFront - Origins](#cloudfront---origins)
  - [CloudFront vs S3 Cross Region Replication](#cloudfront-vs-s3-cross-region-replication)
- [S3 Transfer Acceleration](#s3-transfer-acceleration)
- [AWS Global Accelerator](#aws-global-accelerator)
  - [AWS Global Accelerator vs CloudFront](#aws-global-accelerator-vs-cloudfront)
- [AWS Outposts](#aws-outposts)
  - [Benefits of aws outposts](#benefits-of-aws-outposts)
- [AWS WaveLength](#aws-wavelength)
- [AWS Local Zones](#aws-local-zones)
- [Global Application Architecture](#global-application-architecture)
- [Global Application in AWS - Summary](#global-application-in-aws---summary)
- [Cloud Integration in AWS](#cloud-integration-in-aws)
- [AMAZON SQS - Simple Queue Service](#amazon-sqs---simple-queue-service)
  - [Amazon SQS - FIFO Queue](#amazon-sqs---fifo-queue)
- [Amazon Kinesis](#amazon-kinesis)
- [Amazon SNS (Simple Notification Service)](#amazon-sns-simple-notification-service)
- [Amazon Mq](#amazon-mq)
- [Cloud Integration Section - Summery](#cloud-integration-section---summery)
- [Cloud Monitoring](#cloud-monitoring)
- [Amazon CloudWatch Alarms](#amazon-cloudwatch-alarms)
  - [Amazon CloudWatch Logs](#amazon-cloudwatch-logs)
  - [CloudWatch Logs for EC2](#cloudwatch-logs-for-ec2)
- [Amazon EventBridge](#amazon-eventbridge)
- [AWS CloudTrail](#aws-cloudtrail)
- [AWS X-Ray](#aws-x-ray)
- [AWS CodeGuru](#aws-codeguru)
- [AWS Health Dashboard](#aws-health-dashboard)
- [Cloud Monitoring Summary](#cloud-monitoring-summary)
- [VPC - Virtual Private Cloud](#vpc---virtual-private-cloud)
    - [basic CIDR](#basic-cidr)
  - [VPC - Crash Course](#vpc---crash-course)
- [VPC Networking Summary](#vpc-networking-summary)
- [AWS Shared Responsibility Model](#aws-shared-responsibility-model)
  - [Example: RDS Responsiblity:](#example-rds-responsiblity)
  - [Example: S3](#example-s3)
- [WAF and DDoS Attack protection](#waf-and-ddos-attack-protection)
- [AWS WAF (Web Application Firewall)](#aws-waf-web-application-firewall)
- [AWS Network Firewall](#aws-network-firewall)
- [Encrypted data](#encrypted-data)
- [Data at rest vs Data in transit](#data-at-rest-vs-data-in-transit)
- [AWS KMS (Key Management Service)](#aws-kms-key-management-service)
- [CloudHSM (other service to manage keys)](#cloudhsm-other-service-to-manage-keys)
- [Types of KMS Keys](#types-of-kms-keys)
- [AWS Certificate Manager (ACM)](#aws-certificate-manager-acm)
- [AWS Artifact](#aws-artifact)
- [AWS GuradDuty](#aws-guradduty)
- [Amazon Inspector](#amazon-inspector)
- [AWS Config](#aws-config)
- [Amazon Macie](#amazon-macie)
- [AWS Security Hub](#aws-security-hub)
- [Amazon Detective](#amazon-detective)
- [AWS Abuse](#aws-abuse)
- [Root User Privileges](#root-user-privileges)
- [IAM Access Analyzer](#iam-access-analyzer)
- [Summary: Security and compliance](#summary-security-and-compliance)
- [Amazon Rekognition](#amazon-rekognition)
- [Amazon Transcribe](#amazon-transcribe)
- [Amazon Polly](#amazon-polly)
- [Amazon Translate](#amazon-translate)
- [Amazon Lex and Connect](#amazon-lex-and-connect)
- [Amazon Comprehend](#amazon-comprehend)
- [Amazon SageMaker](#amazon-sagemaker)
- [Amazon Forecast](#amazon-forecast)
- [Amazon Kendra](#amazon-kendra)
- [Amazon Personalize](#amazon-personalize)
- [Amazon Textract](#amazon-textract)
- [Summary - AWS Machine Learning](#summary---aws-machine-learning)
- [AWS Organizations](#aws-organizations)
- [Multi Account Strategies](#multi-account-strategies)
- [Service Control Policies (SCP)](#service-control-policies-scp)
- [SCP Example: Blacklisting and Whitelist Strategies](#scp-example-blacklisting-and-whitelist-strategies)
  - [Example 2](#example-2)
- [AWS Organization - Consolidated Billing](#aws-organization---consolidated-billing)
- [AWS Control Tower](#aws-control-tower)
- [AWS Resource Access Manager (AWS RAM)](#aws-resource-access-manager-aws-ram)
- [AWS Service Catalog](#aws-service-catalog)
- [AWS Pricing Models](#aws-pricing-models)
    - [Pay as you go:](#pay-as-you-go)
    - [Save when you reserve:](#save-when-you-reserve)
    - [Pay less by using more:](#pay-less-by-using-more)
    - [Pay less as AWS Grows](#pay-less-as-aws-grows)
    - [Free services and free tier in AWS](#free-services-and-free-tier-in-aws)
    - [Compute Pricing - EC2](#compute-pricing---ec2)
    - [Compute Pricing - Lambda and ECS](#compute-pricing---lambda-and-ecs)
    - [Storage Pricing - S3](#storage-pricing---s3)
    - [Storage Pricing - EBS](#storage-pricing---ebs)
    - [Database Pricing - RDS](#database-pricing---rds)
    - [Content Delevery pricing - CloudFront](#content-delevery-pricing---cloudfront)
    - [Network Costs in AWS per GB](#network-costs-in-aws-per-gb)
    - [Savings Plan Overview](#savings-plan-overview)
- [AWS Compute Optimizer](#aws-compute-optimizer)
- [Billing and Costing Tools](#billing-and-costing-tools)
  - [AWS Pricing Calculator](#aws-pricing-calculator)
  - [Cost and Usage Reports](#cost-and-usage-reports)
- [Cost Explorer](#cost-explorer)
- [Billing Alarms in CloudWatch](#billing-alarms-in-cloudwatch)
- [AWS Budgets](#aws-budgets)
- [AWS Cost Anomaly Detection](#aws-cost-anomaly-detection)
- [AWS Service Quotas](#aws-service-quotas)
- [AWS Trusted Advisor](#aws-trusted-advisor)
- [AWS Support Plan Pricing](#aws-support-plan-pricing)
  - [Basic Support: Free](#basic-support-free)
  - [Developer Support Plan:](#developer-support-plan)
  - [Business Support Plan (24/7):](#business-support-plan-247)
  - [AWS Enterprise on-Ramp Support Plan (24/7)](#aws-enterprise-on-ramp-support-plan-247)
  - [AWS Enterprise Support Plan (24/7)](#aws-enterprise-support-plan-247)
- [Account best Practices - Summary](#account-best-practices---summary)
  - [Billing and Costing Tools - Summary](#billing-and-costing-tools---summary)
- [AWS STS (Security Token Service)](#aws-sts-security-token-service)
- [AWS Cognito](#aws-cognito)
- [Active Directory](#active-directory)
- [AWS Directory Services](#aws-directory-services)
- [AWS IAM Identity Center](#aws-iam-identity-center)
  - [Advanced Identity - Summary](#advanced-identity---summary)
- [Other AWS Services](#other-aws-services)
  - [WorkSpace vs AppStream](#workspace-vs-appstream)
- [AWS IoT Core](#aws-iot-core)
- [Amazon Elastic Transcoder](#amazon-elastic-transcoder)
- [AWS AppSync](#aws-appsync)
- [AWS Amplify](#aws-amplify)
- [AWS Device Farm](#aws-device-farm)
- [AWS Backup](#aws-backup)
  - [Disaster Recovery Strategies](#disaster-recovery-strategies)
  - [AWS Elastic Disaster Recovery (DRS)](#aws-elastic-disaster-recovery-drs)
  - [AWS DataSync](#aws-datasync)
  - [AWS Application Discovery Service](#aws-application-discovery-service)
  - [AWS Application Migration Service (MGN)](#aws-application-migration-service-mgn)
  - [AWS Migration Evaluator](#aws-migration-evaluator)
  - [AWS Migration Hub](#aws-migration-hub)
  - [AWS Fault injection Simulator (FIS)](#aws-fault-injection-simulator-fis)
- [Step Functions](#step-functions)
- [AWS Ground Station](#aws-ground-station)
- [Amazon Pinpoint](#amazon-pinpoint)
- [AWS Architecting \& Eco-system](#aws-architecting--eco-system)
  - [AWS Cloud Best Practices - Design Principles](#aws-cloud-best-practices---design-principles)
  - [Well Architected Framework 6 Pillars](#well-architected-framework-6-pillars)
    - [1. Operational Excellence](#1-operational-excellence)
    - [2. Security](#2-security)
    - [3. Reliablity](#3-reliablity)
    - [4. Performace Efficiency](#4-performace-efficiency)
    - [5. Cost Optimization](#5-cost-optimization)
    - [6. Sustainability](#6-sustainability)
- [AWS Well-Architected Tool](#aws-well-architected-tool)
- [AWS Cloud Adoption Framework (AWS CAF)](#aws-cloud-adoption-framework-aws-caf)
    - [AWS CAF - Transformation Domains](#aws-caf---transformation-domains)
    - [AWS CAF - Transformation Phases](#aws-caf---transformation-phases)
- [AWS Right Sizing](#aws-right-sizing)
    - [AWS EcoSystem - Free Resources](#aws-ecosystem---free-resources)
    - [AWS EcoSystem - AWS Support](#aws-ecosystem---aws-support)
- [AWS Marketplace](#aws-marketplace)
    - [AWS Training](#aws-training)
  - [AWS Professional Services and Partner Network](#aws-professional-services-and-partner-network)
  - [AWS Knowledge Center](#aws-knowledge-center)
  - [AWS IQ](#aws-iq)
  - [AWS re:Post](#aws-repost)
  - [AWS Managed Services (AMS)](#aws-managed-services-ams)

# Introduction
<!-- deployment modles of the cloud-->
<img src="https://github.com/satyam756/AWS_Cloud_Practitioner/blob/main/images/aws.jpg" height=100 width=100 alt="AWS" />
## Private cloud - rockspace

## public cloude - Azure, Google Cloud, AWS

## Hybrid cloude - mix of both private and public cloud

# Characterstics of cloud computing  

> On-demand self service

> Broad network access

> Multi tenancy and recource pooling : multiple customer can use same network

> Rapid elasticity and scalablity

> Measured service - pay exactly what we use

# Advantages of cloud computing  

> Trade capital expense (capex) for operational expense (opex) -> pay on demand which will reduse the total cost

> benefit from massive ecnomies of scale

> Stop guessing capacity

> increased speed and aglity

> stop spending money running data centers

# problems solved by cloud 

> flexibility - change resource types when needed

> Cost effectiveness - pay as you go for what you use

> Scalablity - accomodates larger loads by making haradware stronger or adding additional nodes

> elasticity - ablity to scale out and scale in

> High availablity and fault tolerance : build across data centers

> Agility - rapidly develop test and launch software applications

# Types of Cloud Computing 

> Infrastructure as a service (IAAS):

* Provides building blocks for cloud it
* provides networking computers, data storage space
* highest level of flexiblity

> Platform as a service(PAAS):

* Removes the need of your organization to manage the underlying infrastructure
* focus on the deployment and management of your application

> Software as a service(SAAS)L

* completly product that is run and managed by the service provider

> Infrastructure as a Service:

    - Amazon EC2 (aws)
    - GCP,Azure,Rackspace,Digital ocen,Linode

> Platform as a Service:

    - Elastic Beanstalk (AWS)
    - Heroku,, Google App Engine(GCP), Windows Azure (microsoft)

> Software as a Service:

    - Many aws services (Rekoginition for machine learning)
    - Google Apps (gmail), Dropbo, zoom

#  Pricing of the cloud

> Aws has 3 pricing fundamentals following - pay as you go pricing

    - Compute: pay for compute time
    - Storage: pay for data stored in the cloud
    - Data Transfer: out of the cloud is paid
        Data transfer in is free

# AWS Cloud History 

> launched in 2002 internally

> 2003 : core strength idea to market amazon infrastructure

> 2004: Launched publicly with SQS

> 2006: re launched publicly with SQS, S3 and EC2

> 2007 : Launched in Europe

<!-- AWS Cloud use cases -->

* AWS enables you to build sophisticated, scalable applications

* Applicable to diverse set of industries

* entrprise IT, Backup n storage, big data analytics

* website hosting, mobile and social apps

* gaming

<!-- AWS Global infrastructure -->

> AWS Regions : all around the world ie us-east

> AWS Availablity Zones : each region has avaiblity zone

> AWS Data Centers: in availablity zones data centers are present

> AWS Edge locations/point of presence: fast content delivery and lower latency

<!-- how to choose aws region -->

> Compliance: with data governance and legal requirments, data never leaves a region without your explicit permission

> proximity to customers: reduced latency

> Available services: new services and new fetures aren't available in every region

> pricing: price varies region to region

<!-- AWS Console used services -->

> Global services:

    - identity and access management (IAM)
    - Route 53 (DNS service)
    - CloudFront (Content Delivery Network)
    - WAF (Web Application Firewall)

> Region Scoped services:

    - Amazon EC2 (IAAS)
    - Elastic Beanstalk (PAAS)
    - Lambda (Function as a service)
    - Rekognition (SAAS)

<!-- Shared Responsiblity Model and aws Acceptable Policy -->

> Customer : Responsible for the security in the Cloud

> Aws: Responsible for the security of the cloud

<!-- Acceptable policies -->

> No illegal harmful or offensive use of contens

> No Security Voilations

> No Network Abuse

> No E-mail or other message Abuse

<!-- Identity Access Management (IAM) -->

# Identity Access Management (IAM)

> it's a Global Service

> root account created by default, shouldn't be used or shared

> Groups: contains only users, users can belongs to multiple groups

> IAM Permission:

    Users or Groups can be assigend json documents called policies

> in aws you apply the least privilege principle, don't give more permission than a user needs

> inline policies -> for a single user does not belongs to group

<!-- IAM Policy Structure -->

> Version: policy language version

> id: identifire for the policy

> statement: one or more individual statements

    - sid: identifire for the statement
    - Effect: allows or deny
    - Principle: Account/user/role for which policty is applied
    - Action: list of actions which policy allows or deny
    - resource list: list of resources to which the action is applied
    - condition: when the policy is in the effect

 <!--IAM Password Policy   -->

> Strong password

> Password Policy:

    - minimum password lenght
    - including uppercase, lowercase, numbers, non alpha numeric chars
    - allow user to change their passwords
    - make users to change the password in some intervals
    - prevent password reuse

> MFA (Multi Factor Authentication)

    - IAM users or atleast Root account must have MFA

> MFA Devices:

    - Virtual MFA Devices: Google Authenticator(phone only), Authy(Multi device)

    - Universal 2nd factor (U2F) security Key: Yubikey (3rd party supported multiple root and iam users in single key)

    - Hardware Key Fob MFA Device: provided by gemalto (3rd party)

    - Hardware Key Fob MFA device for AWS GovCloud (US):
        Provided by SurePassID(3rd party)

<!-- Aws Access Keys, cLI and SDK -->

> To Access AWS you have three options:

    - AWS Management Console: (Protected by password + MFA)
    - AWS Command Line interface (CLI): (Protected by access keys)
    - AWS Software Developer Kit (SDK): for code protected by access keys

<!-- Creation of Access keys for CLI -->

* IAM > Users > Satyam > security credentials >create security key

<!-- Configure AWS CLI -->

* inside aws CLI:

  + aws configure
  + Aws Access Key ID:
  + AWS Secret access Key:
  + Default region name:
  + Default output format:

* aws iam list-users

<!-- Cloud shell as alternative of CLI -->

all linux commands works here

<!-- IAM Roles and Services -->

> Some aws Services will need to perform actions on your behalf

> to do so we will assign permission to aws services with IAM Roles

> Common roles:

    EC2 Instance roles
    Lambda fuction roles
    Roles for CloudFormation

<!-- Create a Role -->

> Types of trusted entity types:

    - AWS Services
    - Aws Account
    - Web Identity
    - SAML 2.0 fedration
    - Custom Trust Policy

> Select AWS Services

    - Use case (EC2)
    - Attatch policy (EC2 Read only policy)
    - Role Name
    - verify the permission
    - create role

<!-- IAM Security Tools -->

> IAM Credentials Report(Account level):

    - a report that lists all your account's users and the staus of their various credentials

> IAM Access Advisor (User-Level):

    - Access Advisor shows the service permissions granted to a user and when those services were last accessed.
    - Can be used to revised the policies

<!-- IAM Best Practices -->

# IAM Best Practices

> Don't use the root account execpt for aws account setup

> one Physical user = One aws User

> Assign users to groups and assign permissions to groups

> Create a strong Password Policy

> Use and enforce the use of MFA

> Create and use Roles for giving permissions to aws servies

> Use access keys and programmatic Access(CLI/SDK)

> Audit permissions of your account using IAM Credendtials Report and IAM Access Advisor

> Never share IAM user and access keys

<!-- Shared Responsibility Model for IAm  -->

> AWS:

    - Infrastructure (Global Network security)
    - Configuration and vulnerablity analysis
    - Compliance validation

> You:

    - Users, Groups, Roles, Policies management and monitoring
    - Enable MFA on all accounts
    - rotate all yours keys often
    - Use IAM tools to apply appropriate permissions
    - Analyze access patterns and review permissions

========================================================

# Amazon EC2

> Ec2 is one of the most popular of AWS offering
> EC2 = Elastic Compute Cloud, IAAS
> it mainly consists in the capability of:

    - Renting virtual machines (EC2)
    - Storing data on virtual drives (EBS)
    - Distributing Load accross the machines (ELB)
    - Scaling the service using Auto-Scaling group (ASG)
# EC2 sizing and configucation options:

> Operating System (OS): Linux, Windows or MAC

> How much compute power and cores (CPU)
> How much random-access memory (RAM)
> How much Storage space:

    - Network-attached (EBS & EFS)
    - Hardware (EC2 Instance store)

> Network Card: Speed of the card, Public IP address
> Firewall rules: Security Group
> Bootstrap Script (Configure at first launch): EC2 User Data Script - script runs only once on the first boot

> Data Script runs with Root (SUDO)

# creating a Instance running linux

#!/bin/bash

# use this for your user data (script from top to bottom)

# install httpd (linux 2 version)

yum update -y

yum install -y httpd

systemctl start httpd

systemctl enable httpd

echo "<h1> Hello World from $(hostname -f)</h1>" > /var/www/html/index.html

<!--- Security Groups -->

> providing the access for the internet also part of networking.

> type | protocol | port range | Source | Destination

# Security Groups:

> can be attatched to multiple instances

> Lokked down to a region/VPC combination

> Does live "outside" the EC2 - if traffic is blocked the ec2 instance won't see it

<!-- Classic ports to know -->

> 22 = SSH

> 21 = FTP

> 22 = SFTP

> 80 = HTTP

> 443 = HTTPS

> 3389 = RDP

<!-- SSH Summary Table -->

> Secure Shell

> Putty - windows

> EC2 instance connect

<!-- SSH EC2 login via MAC/OS X -->

> get the public ip address

> check if port 22 is enable for the SSH

> get the SSH file pem file pek file

> cd /dir of pem file

> ssh -i fileName.pem ec2user@publicIP

> chmod 400 fileName.pem

> ssh -i fileName.pem ec2user@publicIP

> exit or cntrl + d to exit from the shell

<!-- SSH EC2 login via Windows before 10 version -->

> Install Putty

> get the public ip address

> check if port 22 is enable for the SSH

> get the SSH file pem file ppk file

> cd /dir of ppk | ppn file

> if PPk file is not downloaded then use Puttygen

> ec2-user@ipAddress in the url

> SSH > Auth > Private Key File > Browse > select the file and load it

<!-- SSH using Windows 10 -->

> get the public ip address
> check if port 22 is enable for the SSH
> get the SSH file pem file
> cd /dir of ppk | ppn file
> ssh -i fileName.pem ec2-user@publicIP

# SSH Troubleshooting
1. There's a connection timeout

This is a security group issue. Any timeout (not just for SSH) is related to security groups or a firewall. Ensure your security group looks like this and correctly assigned to your EC2 instance.

2. There's still a connection timeout issue

If your security group is properly configured as above, and you still have connection timeout issues, then that means a corporate firewall or a personal firewall is blocking the connection. Please use EC2 Instance Connect as described in the next lecture.

3. SSH does not work on Windows

If it says: ssh command not found, that means you have to use Putty

Follow again the video. If things don't work, please use EC2 Instance Connect as described in the next lecture

4. There's a connection refused

This means the instance is reachable, but no SSH utility is running on the instance

Try to restart the instance

If it doesn't work, terminate the instance and create a new one. Make sure you're using Amazon Linux 2

5.  Permission denied (publickey,gssapi-keyex,gssapi-with-mic)

This means either two things:

You are using the wrong security key or not using a security key. Please look at your EC2 instance configuration to make sure you have assigned the correct key to it.

You are using the wrong user. Make sure you have started an Amazon Linux 2 EC2 instance, and make sure you're using the user ec2-user. This is something you specify when doing ec2-user@<public-ip> (ex: ec2-user@35.180.242.162) in your SSH command or your Putty configuration

6. Nothing is working - "aaaahhhhhh"

Don't panic. Use EC2 Instance Connect from the next lecture. Make sure you started an Amazon Linux 2 and you will be able to follow along with the tutorial :)

7. I was able to connect yesterday, but today I can't

This is probably because you have stopped your EC2 instance and then started it again today. When you do so, the public IP of your EC2 instance will change. Therefore, in your command, or Putty configuration, please make sure to edit and save the new public IP.

Happy troubleshooting!
Satyam

<!-- EC2 instance Connect  -->

> browser based ssh ec2 connect

> Key is not required, it uses temp credentials

> if the SSH is removed from the launch wizard then ssh will not work

> ipv4 and ipv6 both SSH add if ipv4 is not working

# do not add IAM credentials or the secret key

> create a role for that
> aws configure -> while running do not add the user access keys
> attatch the role IAMReadOnly policy

<!-- EC2 Instances Purchasing Options -->

> On-Demand Instance: Short workload, Predictable pricing , pay by second

> Reserved(1 & 3 years): Reserved Instances, Long workloads

    - Convertible Reserved instance: long workloads with flexible instances

> Saving plans (1 & 3 years): Commitment to an amount of usage, long workloads

> Spot instances: short workloads, cheap, can loose instances (less reliable)

> dedicated hosts: book an entire physical server, control instance placement.

> Dedicated instance: no other customer will share your hardware

> Capcaity Reservation: reserver Capacity in a specific AZ for any duration

====================================================

> EC2 on Demand:

    - Pay for what you use
    - linux or windows billing per second after the first minute
    - All other operating systems  - billing per hour
    - has the highest cost but no upfront payments
    - No long-term commitement
    - Recomended for short term and un-intrupted workloads where you can't predict how application will behave

> EC2 Reserved Instances:

    - up to 72% discount compared to on-demand
    - you reserve a specific instance attribute (instance type, Region, Tenancy, OS)
    - Reservation Period: 1 year(+discount) or 3 years (+++discount)
    - payment option: no upfront(+),partial upfront(++), all upfront(+++)
    - Reserved Instance Scope: Regional or zonal
    - Recomended for Stedy-state usage applications
    - you can buy and sell in reserved instance marked places.

> Convertible Reserved instance:

    - can changed the ec2 instance type, instance family,os, scope and tencancy
    - up to 60% discounts

> Savings plans:

    - Get discount based on long -term usage(up to 72% same as reserved instances)
    - commit to certain type of usage ($10/hour for 1 or 3 years)
    - usage beyond ec2 savings plans is billed at the on demand price
    - Locked to a specific instance family and aws region
    - flexible accross:
        instance size, os , tenancy(host dedicated as default)

> EC2 Spot Instances:

    - can get a discount of up to 90% compared to on demand
    - instances that you can lose at any point of time if  your maz prize is less than the current spot price
    - the most cost efficient instance in aws
    - useful to workload that is resilient to failure
        * Batch jobs
        * data analysis
        * Image processing
        * any distributed workloads
        * workloads with a flexible start and end time
    - not suited for critical jobs or databases

> EC2 Dedicated Host:

    - a physical server with ec2 instance capicity fully dedicated to your use
    - allows  you address compilance requirements and use your existing server-bound software licences
    - Purchasng option:
        * on-demand = pay per second
        * reserved =  1 or 3 years (no upfront,partial upfront, all upfront)
    - the most expensive option
    - useful for softwares that have complicated licensing model
    - or for companies that have strong regulatory or compliance needs

> EC2 Dedicated instances:

    - Instance run on hardware that's dedicated to you
    - May share hardware with other instances in same account
    - No control over instance placement(can move hardware after stop/start )

> EC2 Capicity Reservation:

    - Reserves on demand instances capacity in a specific AZ for any duration.
    - you always have access to ec2 capacity  when you need it
    -  no time commitment, no billing discounts
    - combine with regional reserved instances and savings plans to benefit from billing discounts
    - charged at on-demand whether you run you run instances or not
    - Suitable for short-term, uninterrupted workloads that needs to be in a specific Az

<!-- Shared Responsiblity model for EC2 and users -->

> AWS:

    - Infrastructure (Global newtwork security)
    - isolation on physical hosts
    - Replacing faulty hardware
    - Complicance validation

> User:

    - Security Groups rules
    - operating system patches and updates
    - Software and utlities installed on the ec2 instance
    - IAM roles assigned to EC2 and iam user access management
    - Data security on your instances

<!-- Instance storage -->

# EBS (Elastic Block store)

> EBS is a network drive you can attatch to your instance while they run

> it allows your instances to presist data even after termination

> they can only be mounted to one instance at a time (at CCP level (certified cloud practioner))

> they are bound to a specific availablity zone

Analogy: Network USB Stick

> it's a network drive (not a physical drive)

> it uses nework to communicate the instance which means there might be a bit of latency

> it can be detached from an en2 instance and attatched to one quickly

> it's locked to an az

    - to move a volume across, you first need to snapshot it

> have a provisioned capacity (Size in GBs and iops)

    - you get billed for all the provisioned capacity
    - you can increase the capacity of the drive over time

> EBS - Delete on termination attribute:

    - controls the EBS behaviour when ec2 instance terminates
    - by default the root volume EBS is deleted
    - by default any other attatched volume is not deleted
    - can be controlled by aws console/ aws CLI
    - use case: preserve the root volume when instance terminated
# About EBS Multi-Attach

While I say that in the previous lecture that EBS volumes cannot be attached to multiple instances, I know it is not true for io1 and io2 volume types: this is called the EBS Multi-Attach feature.

From an AWS Cloud Practitioner exam perspective this out of scope for the exam.
In order to keep the course simple and accessible, I have left out this feature from the course.

If you are curious to learn about EBS Multi-Attach, you will find it in the AWS Certified Solutions Architect Associate course, or in the AWS documentation.
[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes-multi.html]

<!-- EBS Snapshots (backup) -->

> Make a backup of your EBS vloume an a point in time

> Not necesary to detatch volume to do snapshot but recomended

> can copy snapshots across Az regions

<!-- features of EBS -->

> EBS snapshots Archive:

    - Move a snapshot to an "Archive tier" that is 75% cheapr
    - Takes within 24 to 72 hours for restoring the archive

> Recycle bin for EBS snapshots:

    - Setup rules to retain deleted snapshots so you can recover them after an accidental deletion
    - specify retention (from 1 day to 1 year)

> can create retention rule on accidental deletion on snapshot in recycle bin

> to restore have to wait for 24 to 72 hours in archival

<!-- AMI overview -->

# Amazon Machine Image

> AMI are a custimization of an EC2 instance

> AMI are built for a specific region

> you can launch EC2 instance from:

    - A public AMI : AWs provided
    - Your own AMI : You make and maintain them yourself
    - An AWS Marketplace AMI: An ami someone else made

> AMI Process (from an EC2 Instance):

    - Start an EC2 Instance and Customize it
    - Stop the instance (For Data Integrity)
    - Build AMI: this will also creats EBS Snapshots
    - Launch instances from other AMI's

<!-- EC2 Image Builder -->

> Used to automate the creation of virtual machines or container images

> => Automate the creation, maintain, validate and test ec2 ami's

> ec2 image builder -> create -> builder ec2 instance -> new AMI -> test ec2 instance -> Ami is distributed (multiple regions)

> it can be run on schedule

> it's free service (only pay for the underlying resources)

<!-- EC2 Instance store -->

> EBS volumes are network drives with good "limited" Preformance

> if you need a high performance hardware disk, use ec2 instance store

> better i/o performance

> ec2 instance store lose their storage if they're stopped

> good for buffer/ cache/ scratch data/ temporary content

> risk of data loss if hardware fails

> Backup and replication are your responsiblity

> Local ec2 instance store

# EFS - Elastic File System

> Managed NFS (Network file system) that can be mounted on 100s of ec2

> EFS works with linux ec2 instances in multi-AZ

> Highly availale scalable expesive (3Xgp2), pay per use no capacity planning

<!-- EFS infrequent Access (EFS-IA) -->

> Storage class that is cost optimized for file not accessed every day

> Up to 92% lower cost compared to EFS Standards

> EFS will automatically ove your files to EFS-IA based on the last time they were accessed

> Enable EFS-IA with a lifeCycle Policy

> Example: move files that are not accessed for 60 days to EFS-IA

> Transparent to the application accessing EFS

<!-- Shared responsiblity for EC2 storage -->

> AWs:

    - Infrastructure
    - Replication for data for EBS volume and EFS drives
    - Replacing Faulty hardware
    - Ensuring their employee cannot access your data

> Customer:

    - Setting up backup/snapshot procedures
    - setting up data encryption
    - Responsiblity of any data on drives
    - understanding the risk of using ec2 instance store

<!-- Amazon FSx -->

* Launch 3rd party high performace file system on aws
* Fully managed as service
* FSx for Lustre, FSx for windows file server, FSx for NetApp ONTAP

> Amazon FSx for Windows File Server:

    - A fully managed, highly reliable and scalable windows native shared file system
    - Built on windows file server
    - Support SMB protool and windows NTFS
    - integrated with microsoft active directory
    - can be accessed from aws or your on-premise infrastructure

> Amazon FSx for Lustre:

    - A fully managed high performance scalable file storage for high performance computing (HPC)
    - the name Lustre is derived from linux and cluster
    - machine learning, analytics, video processing, financial modeling...
    - Scales upto 100s GB/s, millions of IOPS, sub-ms latencies

<!-- Scalability and high availablity -->

> Scalablity means that an application/system can handle grater loads by adapting

> two kinds of scalablity:

    - Vertical Scalablity
    - Horizontal Scalablity

> Scalablity is linked but different to high availablity

# Vertical Scalablity:
    - vertical scalablity means increasing the size of the instance
# Horizontal Scalablity:
    - Horizontal scalablity means increasing the number of instances/systems for your application
# High availablity:
    - High availablity usually goes hand in hand with horizontal scaling
    - Running your application/system in at least 2 availablity zones
    - goal is to survive a data center loss

> Vertical scaling:

    - Increase instance size(=scale up / down)
    - from t2.nano - 0.5G of RAM, 1 vCPU
    - to u-12tb.metal - 12.3TB of RAM, 448 vCPUs

> Horizontal Scaling:

    - increase number of instances (=scale out /in)
    - Auto Scaling Group
    - Load Balancers

> High Availablity:

    - Run instances for the same applications across multi AZ's
    - Auto Scaling Group Multi AZ's
    - Load balancers in Multi AZ's
# Scalablity vs Elasticity (vs Agility)
* Scalablity:
  ability to accommodate a larger load by making the hardware stronger(scale up), or by adding nodes (scale out)

* Elasticity:
  once a system is scalable, elasticity means that there will be some "Auto Scaling" so that the system can scale based on the load. this is "Cloud Friendly": pay-per-use, match demand, optimize costs

* Agility:
  (not releted to scalablity - distractor) new IT resources are only a click away, which means that you reduce the time to make those resource available to your developers from weeks to just minutes.

## what is load balancing:

> Load balancers are server that forward internet traffic to multiple servers (EC2 instances) downstream.

# why use a load balancers:

    > spread load across multiple downstream instances
    > expose a single point of access (DNS) to your application
    > seamlessly handle failures of downstream instances
    > Do regular health checks to your instances
    > provide SSL terminations (HTTPS) for your websites
    > High availablity across zones

> An ELB (Elastic Load Balancer) is managed load balancer

    - AWS guarntees that it will be working
    - AWS takes care of upgrade, maintenance, high availablity
    - AWS provides only a few configuration knobs

> it costs less to setup your own load balancer but it will be a lot more effort on your end(maintenance, integration)

> 4 kinds of load balancers offered by AWs:

    - Application Load Balancer(HTTP/HTTPS only) - Layer 7
    - Network Load Balancer(ultra-high performance,allows for TCP and UDP) - Layer 4
    - Gateway Load Balancer - Layer 3
    - Classic Load Balancer (retired in 2023) - Layer 4&7
# ALB (Application load balancers):

> HTTP/HTTPS/gRPC protocols

> HTTP Routing features

> Static DNS (URL)

# NLB (Network load balancers):

> TCP/UDP Protocols

> High performance: Millions of request per seconds

> Static IP through Elastic IP

# GLB (Gateway load balancers):

> GENEVE Protocol on IP Packets (Layer 3)

> Route traffic to firewalls that you manage on ec2 instances

> intrusion Detection

> 3rd party security virtual appliances

# Auto Scaling Group:

> In real life, the load on your websites and application can change

> in cloud you can create and get rid of servers very quickly

> the goal of an Auto Scaling Group (ASG) is to:

    - Scale out (Add ec2 instances) to match an increased load
    - Scale in (remove ec2 instances) to match decreased load
    - ensure we have minimum and maximum number of machines running
    - Automatically register new instances to load balancer
    - Replace unhealthy instances

> Cost savings: Only run at an optimal capacity (principle of the cloud)

# Scaling Strategies
* Manual Scaling:
  Update the size of ASG Manually

* Dynamic Scaling:
  Respond to Changing demand

  + Simple/step scaling:
    - when a cloud watch alarm is triggered then add 2 units (CPU > 70%)
    - when a cloud watch is triggered then remove(CPU < 30%)
  + Target Tracking Scaling:
    - example: i want the average ASG CPU to stay at around 40%
  + Scheduled Scaling:
    - Anticipate a scaling based on known usage patterns.
    - example: increase the min.capacity to 10 at 5 pm on fridays.

* Predictive Scaling:

  + Uses Machine learning to predict future traffic ahead of time

  + Automatically provisions the right number of EC2 instances in advance

  + useful when your load has predictable time-based patterns

> for the cleanup delete the ASG and load balancers

<!-- Amazon S3 -->

> Amazon S3 is one of the main building blocks of AWS

> it's Advertised as "infinity Scaling" Storage

> Many Websites use Amazon S3 as a backbone

> Many aws Services use Amazon S3 as an integration as well

# Amazon S3 uses Cases

> Backup and Storage

> Disaster Recovery

> Archive

> Hybrid Cloud Storage

> Application hosting

> Media hosting

> Data lakes and big data analytics

> Software delivery

> Static Website

* Nasdaq Stores 7 years of data into s3 Glacier

* Sysco runs analytics on it's data and gain business insights

## Amazon S3 Buckets:

> Amazon s3 allows people to store objects(files) in "buckets"(directories)

> Bucket must have globally unique name(across all regions all accounts)

> buckets are defined at the region level

> S3 looks like a global service but buckets are created in a region

> Naming conventions:

    - No Uppercase, No underscore
    - 3-63 character long
    - Not an IP
    - Must start with lowercase letter or number
    - Must not start with the prefix xn--
    - Must not end with the suffix -s3alias

> Objects (files) have a key
> the key is the full path:

    - s3://my-bucket/my_file.txt (key is full path)

> the key is composed of prefix + object name

> there's no concept of "directories" within buckets

> just keys with very long names that contains (/) slashes

## Amazon S3 - objects (cont):

> Object values are the content of the body:

    - Max Object size is 5TB (5000GB)
    - if uploading more that 5GB, must use "multi-part upload"

> Metadata(list of text key / value pairs - system or user metadata)

> Tags (Unicode Key / value pair - upto 10) - useful for security / lifecycle

> Version ID (if versioning is enabled )

<!-- Creating Amazon S3 bucket -->

> create and upload folders and files inside S3

> Delete the objects

<!-- Amazon S3 - Security -->

* User Based:

  + IAM Policies: Which api calls should be allowed for a specific user from IAM

* Resource based:

  + Bucket policies: bucket wide rules from S3 console - allows cross account
  + object Access Control List(ACL): finer grain (can be disabled)
  + Bucket access control list (ACL): less common (can be disabled )

* an IAM principle can access an S3 object if:

  + the user IAM permission allow it or the resource policy allows it
  + And ther's no explicit deny

* Encryption: encrypts objects in amazon S3 using encryption keys

<!-- S3 Bucket Ploicy -->

* Json Based Policies:
  + Resource: Bucket and objects
  + Effect: Allow/Deny
  + Action: Set of API to Allow or Deny
  + Principal: the account or user to apply the policy to

ex:
`[{
"Version": "2012-10-17", 
"Statement": {
"Sid": "PublicRead", 
"Effect": "Allow", 
"Principal": "_", 
"Action": [
"s3: GetObject"
], 
"Resource": [
"arn:aws:s3:::examplebucket/_"
]
}
}]`

## Use S3 Bucket for policy to:

* Grant public access to the bucket
* force objects to be encrypted at upload
* grant access to another account(Cross Account)

* Bucket settings for block public Access:

* Block all public access: On
* Block public access to buckets and objects granted through new access control list (ACL's): On
* Block public access to bucktes and objects granted through any access control access list (ACL's): On
* Block public access to bucktes and objects granted through new public bucket or access point policies: On
* Block public access to bucktes and objects granted through any public bucket or access point policies: On
# use Policy generator to create a json file

<!-- Amazon S3 Versioning -->

* you can version your files in Amazon S3
* it is enabled at the bucket level
* same key overwrite will change the "version":1, 2, 3...
* it is best practice to version your buckets:

  + protect against unintended deletes
  + easy roll back to the previous version

* Any file that is not versioned prior to enabling versioning will have version "null"
* suspending versioning does not delete the previous versions.

> use show versions to see the versions

<!-- S3 Replication in AWS -->

> 2 types of Replications:

    1) CRR: Cross Region Replication
    2) SRR: Same Region Replication

> Must enable versioning in source and destination buckets

> Buckets can be different AWS Accounts

> Copying is Asynchronous

> Must give proper IAM Permission to S3

* Use Cases:
  + CRR: Compliance, lower latency access, replication accross accounts
  + SRR: log aggregation, live replication between production and test accounts

* Management > Replication Rule > apply all objects in bucket >chose the region

<!-- Storage Classes in S3 -->

> Amazon S3 Standard - General Purpose

> Amazon S3 Standard-Infrequent Access (IA)

> Amazon S3 One Zone-Infrequent Access

> Amazon S3 Glacier Instant Retrieval

> Amazon S3 Glacier Flexible Retriveal

> Amazon S3 Glacier Deep Archive

> Amazon S3 Intelligent Tiering

> Can move between classes manually or using S3 Lifecycle configurations

<!-- S3 Durablity and Availablity -->

> Durablity:

    - High durablity (99.99999999999, 11 9's) of object across multiple AZ
    - if you store 10,000,000 objects with amazon S3, you can on average expect to incur a loss of a single object once every 10,000 years
    - same for all storage class

> Availablity:

    - Measures how readily available a service is
    - Varies depending on storage class
    - Example: S3 standard has 99.99% availablity = not available 53 minutes a year.

==========================================================

> Amazon S3 Standard - General Purpose:

    - 99.99% Availablity
    - Used for frequently accessed data
    - Low Latency and high throughput
    - Sustain 2 Concurrent facility failures

> Use cases:

    - Big Data Analytics, Mobile and gaming applications, content distribution..

-

> Amazon S3 Standard-Infrequent Access (IA):

    - for data that is less frequently accessed, but requires rapid access when needed
    - Lower cost than S3 Standard
    - 99.9% Availablity

> Use cases:

    - Disaster Recovery, backups

-

> Amazon S3 One Zone-Infrequent Access:

    - High durablity (99.999999999%) in a single AZ
    - Data lost when AZ is Destroyed
    - 99.5% Availablity

> Use cases:

    - Storing Secondary backup copies of on-premise data or data you can re-create

-

> Amazon S3 Glacier Storage Classes:

    - Low cost object storage meant for archiving/backup
    - Pricing: price per storage + object retrieval cost

> Amazon S3 Glacier Instant Retrieval:

    - Miliseconds retrival, great for data accessed once a quarter
    - Minimum storage duration 90 days

> Amazon S3 Glacier Flexible Retriveal :

    - Expedited (1 to 5 minutes), standard (3 to 5 hours), bulk(5,12 hours) - free
    - Minimum storage duration 90 days

> Amazon S3 Glacier Deep Archive:

    - Standard (12 hours), Bulk(48 hours)
    - Minimum storage duration is 180 days

-

> Amazon S3 Intelligent Tiering:

    - Small monthly monitoring and auto-tiering fee
    - Moves objects automatically between access tiers based on usage
    - there is no retrieval charges in S3 intelligent-Tierung

> Frequent Access Tier(Automatic): Default Tier

> Infrequent Access Tier(Automatic): Object not accessed for 30 days

> Archive instant Access Tier(Automatic): Objects not accessed for 90 days

> Archive Access Tier(Optional): Configurable from 90 days to 700+ days

> Deep Archive Access Tier(Optional): Configurable from 180 days to 700+ days

<!-- S3 Encryption -->

> Server-Side Encryption:

    - When user uploads an object/Files to S3 bucket after upload Amazon encrypts the object/Files

> Client-side Encryption:

    - before uploading to S3 Bucket user encrypts the object/Files

<!-- IAM Access Analyzer for S3 -->

> Ensures that only intended people have access to your S3 Buckets

> Example: Publicly accessible bucket, bucket shared with other aws account

> Evalutes S3 Bucket Policies, S3 ACL's, S3 Access Point Policies

> Powered by IAM Access Analyzer

<!-- Shared Responsiblity Model for S3 -->

> AWS:

    - Infrastructure (Global Security,Durablity,availablity,sustain concurrent loss of data in two facilities)
    - Configuration and vulnerablity analysis
    - Compliance Validation

> User:

    - S3 versioning
    - S3 Bucket Policies
    - S3 Replication Setup
    - Logging and monitoring
    - S3 Storage Classes
    - Data encryption at rest and in transit

==========================================================

# AWS Snow Family

> Highly-Secure, Portable devices to collect and process data at the edege and migrate data into and out of aws

> For Data Migration:

    1) SnowCone
    2) Snowball Edge
    3) Snowmobile

> For Edge Computing:

    1) SnowCone
    2) Snowball Edge

> Note: AWS Snow Family is offline devices to perform data migration, if it takes more than a week to transfer over the network, use Snowball Devices!

* Snowball Edge (For Data Transfers):
  + Physical data transport solution: Move TBs or PB's of data in or out of aws
  + Alternative to moving data over the network(and paying network fees)
  + pay per data transfer job
  + Provide block storage and amazon s3 compatible objct storage

* Snowball edge storage optimized: \* 80TB of HDD capacity for block volume and s3 compatible object storage
* snoball edge Compute optimized \* 42TB of HDD or 28TB NVM'e capacity for block volume and s3 compatible object storage

> Use cases:

* large data cloud migration, DC: dcommission, disaster recovery

## AWS SnowCone and SnowCone SSD

> Small portable computing, anywhere rugged and secure withstands hard environments

> light (4.5 pounds, 2.1 KG)

> device used for edge computing storage and data transfer

> SnowCone - 8TB of HDD Storage

> SnowCone SSD - 14TB of SSD Storage

> use SnowCone where Snowball does not fit(space constrained environment)

> must provide your own battery / Cables

> Can be sent back to aws offline or connect it to internet and use AWS DataSync to send data.

## AWS Snowmobile

> Transfer exabytes of data (1 EB = 1000PB = 1000, 000TB's)

> each Snowmobile has 100PB of capacity (use multiple in parallel)

> High security: temperature Controlled, GPS, 24/7 video surveillance

> Better than Snowball if you transfer more than 10 PB

# AWS Snow Family for Data Migration

> SnowCone:

* Storage Capacity: 8TB HDD and 14TB SSD
* Migration Size: up to 24TB online and offline
* DataSync agent: Pre-installed

> Snowball Edge:

* Storage Capacity: 80TB Usable
* Migration Size: up to petabytes offline
* DataSync agent: N/A

> SnowMobile:

* Storage Capacity: <100PB
* Migration Size: up to exabytes, offline
* DataSync agent: N/A
# Snow Family - Usage process

> Request Snowball devices from the aws console for delivery

> install the snowball client / AWS OpsHub on your servers

> Connect the snowball to your servers and copy files using the client

> ship back the device when you're done(goes to the right aws facility)

> Snowball is completely wiped

# for SnowBall Edge computing

> Process data while it's being created on an edge location
> ex: a truck on the road, a ship on the sea, a mining station underground

> these locations may have:

    - limited/no internet access
    - limited/no easy access to computing power

> we setup a snowball edge/snowcone devices to do edge computing

> use cases for edge computing:

    - preprocess data
    - Machine learning at the edge
    - Transcoding media streams

> Eventually we can ship back the device to aws.

* > SnowCone and SnowCone SSD(smaller):

  + 2 CPU's, 4GB of memory wired/wireless access
  + USB-C power using cord or the optional battery

> SnowBall Edge - Compute optimized:

    - 104 vCPU,416 GiB of RAM
    - optional GPU (useful for video processing or machine learning)
    - 28TB NVMe or 42TB HDD usable storage
    - Storage clustering available (up to 16 nodes)

> SnowBall Edge - Storage Optimized:

    - up to 40 vCPUs,80 GiB of RAM, 80 TB storage
    - All can run EC2 instances and AWS Lambda functions (using AWs IoT Greengrass)
    - Long term deployment options 1 and 3 years discounted pricing
# AWS OpsHub

> Historically, to use Snow Family devices, you needed a CLI(Command Line Interface Tool)

> Today you can use AWS OpsHub (a software you install on your computer / laptop) to manage your Snow Family device

* Unlocking and configuring single or clustered devices
* Transferring files
* launching and managing instances running on Snow family devices
* monitor device matrics (storage capacity, active instances on your devices)
* launch compatible aws services on your devices
# Snowball edge pricing

> You pay for device usage and data transfer out of aws

> Data transfer IN to amazon S3 is free

> On-Demand:

    - include a one time service fee per job which includes:
    - 10 days usage for Snowball edge storage optimized 80 TB
    - 15 days usage for Snowball edge storage optimized 210 TB
    - Shipping days are not counted towards the included 10 or 15 days
    - pay per day for any additional days

> Committed upfront:

    - pay in advance for monthly, 1-year and 3 year of usage (Edge Computing)
    - up to 62% discounted pricing
# AWS Storage Gateway

> AWS is pushing for "Hybrid Cloud" :

    - Part of your infrastructure is on premises
    - Part of your infrastructure in on the cloud

> this can be due to:

    - Long cloud migrations
    - Security requirements
    - Compliance requirements
    - IT strategy

> S3 is a proprietary storage technology (unlike EFS/NFS), so how do you expose the S3 data on-premise?

> AWS Storage Gateway!

# AWS Storage Cloud Native Options:

> Block:

    - Amazon EBS
    - EC2 Instance Store

> File:

    - Amazon EFS

> Object:

    - Amazon S3
    - Amazon Glacier

> Storage gateway allows you to bridge between on-premise data and cloud data in S3

> Hybrid storage service to allow on-premises to seamlessly use the aws cloud

> use case:

    - disaster recovery, backup and restore, tiered storage

## Types of Storage gateways:

> File Gateway
> Volume Gateway
> Tape Gateway

<!-- AWS Databases -->

> Storing data on disk (EFS, EBS, EC2 instance store, S3) can have it's limits

> Somtimes you want to store data in database.

> you can structure the data

> you build indexes to efficiently query / serch through the data

> you define relationships between your datasets..

<!-- Database and shared responsibility on aws -->

> AWS offers use to manage different databases

> Benefits include:

    - quick provisioning,High availablity,vertical and horizontal scaling
    - Automated backup and restore,Operations, upgrades
    - Operating system patching is handled by aws
    - Monitoring alerting

> Note: Many databases technologies could be run on EC2, but you must handle yourself the resiliency, backup, patching, high availablity, falut tolerance, scaling etc...

# AWS RDS

> RDS stands for Relational Database service

> it's managed DB services for DB use SQL as a query language.

> it allows you to create databases in the cloud that are managed by AWS

> below are some databases:

    - Postgres
    - MySQL
    - MariaDB
    - Oracle
    - Microsoft SQL Server
    - Aurora (AWS proprietart database)

## Advantages over RDS vs deploying DB on EC2:

> RDS is managed service

> Automated provisioning, OS patching

> Continuous backups and restore to specific timestamp (point in time restore)

> Monitoring dashboards

> Read replicas for improved read performace

> Multi AZ setup for DR(Disaster Recovery)

> Maintenance windows for upgrade

> Scaling Capability (Vertical and Horizontal)

> Storage backed by EBS (gp2 or io1)

> Cannot use SSH into RDS because it's handled by AWS

# Amazon Aurora

> Aurora is proprietary technology from aws(not open sourced)

> PostgreSQL and MySQL are both supported by Aurora DB

> Aurora is "AWS Cloud Optimized" and claims 5x performance improvement over MySQL on RDS, over 3x the performance of Postgres on RDS

> Aurora storage automatically grows in increments of 10GB, up to 128 TB

> Aurora costs more than RDS(20% more) - but is more efficient

> Not in Free Tier

# Amazon Aurora Serverless

> Automated database instantiation and auto scaling based on actual usage

> PostgreSQL and MySQL are both supported as Aurora serverless DB

> No Capacity planning needed

> Least management overhead

> Pay per Second, can be more cost-effective

> use cases:

    - good for infrequent, internittent or unpredictable workloads

<!-- RDS Deployment Options -->

> Read Replicas:

    - Scale the read workloads of your DB
    - can Create up to 15 Read Replicas
    - Data is written only in the main DB

> Multi AZ's (Avaliblity Zones):

    - Failover in case on AZ outage (High availablity)
    - Data is only read/written to the main database
    - can only have 1 other AZ as failover

> Multi Region (Read Replica):

    - Scale the read workloads of your DB in Multi Region
    - Disaster Recovery in case of region issue
    - Local performance for global reads
    - Replication Cost between network transfer
# Amazon ElastiCache Overview:

> The same way RDS is to get managed Relational Databases.

> ElastiCache is to get managed Redis or Memcached

> Caches are in-memory databases with high performance, low latency

> Helps reduce load off databases for read intensive workloads

> AWS Takes care of OS maintenance / patching, optimization , setup configuration, monitoring, failure recovery and backups

# Dynamo DB

> Fully Managed and highly available with replication across 3 AZ's

> NoSQL Database - not a relational database

> Scales to massive workloads, distributed "serverless" database

> Millions of request per seconds, trillions of row, 100s of TB of storage

> Fast and consistent in performance

> Single-digit millisecond latency - low latency retrieval

> Integrated with IAM for security, authorization and administration

> Low Cost and auto scaling capablities

> Standard and infrequent access (IA) Table class

> DynamoDB is a key/value database

## DynamoDB Accelerator - DAX

> Fully managed in-memory cache for Dynamo DB

> 10x performance improvement - single-digit millisecond latency to microseconds latency - when accessing your Dynamo DB tables

> secure, highly scalable and highly available

> Difference with ElastiCache at the CCP level:

    - DAX is only used for and is integrated with DynamoDB
    - ElastiCache can be used for other databases

> DynamoDB - Global Tables:

    - Make a DynamoDB Tables accessible with low latency in multiple regions
    - Active-Active replication (Read/write to any aws region)
# Redshift database

> Redshift is based on PostgreSQL, but it's not used for OLTP (online Transaction Processing)

> it's OLAP (Online Analytical Processing), analytics and data warehousing

> Load Data once every hour, not every second

> 10x better performance than othet data warehouses, scales to PB's of data

> Columnar Storage of data (insted of row based)

> Massively Parallel Query Execution (MPP), highly available

> Pay as you go based on the instances provisioned

> Has a SQL interface for performing the queries

> BI (Business Inteligence) tools such as AWS Quicksight or Tableau intergarate with it

# Redshift Serverless

> Automatically provisions and scales data warehouse underlying capacity

> Run analytics workloads without managing data warehouse infrastrusture

> Pay only for what you use (save costs)

> Use Cases:

    - Reporting
    - Dashboarding Applications
    - Real-time Analytics..

> Enable Amazon Redshift serverless for your aws account

               |

> Connect using amazon redshift query editor or any other tool

               |

> Amazon Redshift serverless: run queries by automatically provision and scale capacity based on workloads

                |

> Pay only for compute and storage used during analysis

# Amazon EMR (Elastic MapReduce):

> EMR stands for Elastic MapReduce

> EMR helps creating Hadoop clusters (Big Data) to analyze and process vast amount of data

> The clusters can be made of hundereds of EC2 instances

> Also supports Apache Spark, HBase, Presto, Flink...

> EMR takes care of all the provisioning and configuration

> Auto-Scaling and integrated with Spot instances

> Use Cases:

    - Data processing
    - Machine Learning
    - Web indexing
    - Big Data..
# Amazon Athena:

> Serverless query to perform analytics against S3 objects

> Uses standard SQL language to query the files

> Supports CSV, JSON, ORC, Avro and Parquet (built on Presto)

> Pricing: $5.00 per TB of data scanned

> Use compressed or columnar data for cost-saving (less scan)

> use cases:

    - Business intelligance
    - Buiness Analytics/reporting
    - Analyze and query VPC flow logs, ELB logs
    - CloudTrail trails..
# Amazon QuickSight

> BI in AWS

> Serverless machine learning-powered business intelligence service to create interactive dashboards

> Fast, automatically scalable, embeddable, with per-session pricing

> use Cases:

    - Business analytics
    - Building visualizations
    - perform ad-hoc analysis
    - get business insights using data

> integrated with RDS, Aurora, Athena, Redshift, S3...

# DocumentDB:

> Aurora is an "AWS-implementation" of PostgreSQL/MySQL..

> DocumentDB is the same for MongoDB(which is noSQL DB)

> MongoDB is used to store, query, and index JSON Data

> Similar "deployment concepts" as Aurora

> Fully Managed, highly available with replication across 3 AZ's

> DocumentDB storage automatically grows in increments of 10GB up to 64TB

> Automatically scales to workloads with millions of request per seconds

# Amazon Neptune:

> Fully managed graph database

> A popular graph dataset would be a social network:

    - users have friends
    - posts have comments
    - Comments have likes from users
    - users share and like posts

> Highly available across 3 AZ's with upto 15 read replica's

> Build and run applications working with highly connected datasets

> optimised for complex and hard queries

> can store up to billions of relations and query the grapth with milliseconds latency

> use cases:

    - Great for Knowledge graphs (Wikipedia)
    - Fraud detection
    - Recommendation engines
    - Social networking
# Amazon QLDB (Quantum ledger Database)

> QLDB - Quantum ledger Database

> A ledger is a book recording financial transactions

> Fully managed, serverless, high available, replication accross 3 AZ's

> used to review history of all the changes made to your application data over time

> immutable system: no enty can be removed or modified, cryptographically verifiable

> 2-3x better performance than common ledger blockchain framework, manipulate data using SQL

> Difference with Amazon Managed Blockchain: No decentralization component in accordance with financial regulation rules

# Amazon Managed Blockchain:

> Blockchain makes it possible to build application where multiple parties can execute transactions without the need for a trusted, central authority

> Amazon Managed Blockchain is managed service to :

    - Join public blockchain networks
    - or create your own scalable private network

> Compatible with the frameworks Hyperledger Fabric and Ethereum

# AWS Glue:

> Managed extract, transform, and load(ETL) service

> Useful to prepare and transform data for analyics

> Fully serverless service

> extracts the data from S3/RDS -> extract(transform) -> load -> RedShift/other DB's

> Glue data Catalog:

    - catalog of datasets
    - can be used by Athena,RedShift, EMR
# DMS - Database Migration Service

> Quickly and securely migrate databases to aws, resilent, self healing

> the source database remains available during the migration

> supports:

    - Homogeneous migration: oracle to oracel (same DB's)
    - Heterogeneous migration: Microsoft SQL Server to Aurora

> Summary:

* Relational Databases - OLTP: RDS and Aurora(SQL)
* Difference between Multi AZ, Read Replica, Multi-region
* in-memory Database: ElastiCache
* key/value database: DynamoDB
* DAX: Cache for DynamoDB
* warehouse - OLAP: Redshift(SQL)
* Hadoop Cluster: EMR
* Athena: Query data on Amazon S3(serverless and SQL)
* QuickSight: Dashboards on your data(serverless)
* DocumentDB: "Aurora for MongoDB" (JSON - NoSQL)
* Amazon QLDB: Financial Transaction ledger(immutable)
* Amazon managed Blockchains: Managed hyperledger fabric and ethereum blockchains
* Glue: Managed ETL (Extract, transform, load) and data catalog service
* Database migration: DMS
* Neptune: Graph database

<!-- Other Compute services -->

# Docker

> Docker is a software development platform to deploy apps

> apps are packaged in containers that can be run on any OS

> Apps run the same, regardless of where they're run:

    - Any Machin
    - No Compatiblity issues
    - Predictable behaviour
    - less work
    - Easier to maintain and deploy
    - Works with any language,any OS,Any technology

> Scale containers up and down very quickly

> Docker images are stored in Docker repo's

# ECS - Elastic Container Service:

> ECS - Elastic Container Service

> Launch docker containers on AWS

> you must provision and maintain the infrastructure

> AWs takes care of starting/stopping containers

> has integration with the application load balancer

# Fargate

> Lunch Docker containers on AWS

> you do not provision the infrastructure - simpler

> Serverless offering

> AWS just runs containers for you based on the CPU/RAM you need

# ECR - Elastic Contianer Registry

> Elastic Container Registry

> Private Docker Registry on AWS

> this is where you store your docker images so they can be run by ECS or fargate

 <!-- Serverless -->

# Lambda:

> Easy pricing:

    - Pay per request and compute time
    - Free tier of 1,000,000 aws lambda request and 400000 gb's of compute time

> Integrated with the whole aws suite when needed

> event driven: functions get invoked by aws when needed

> integrated with many programming languages

> easy monitoring through aws cloudwatch

> easy to get more resources per functions (up to 10gb of RAM)

> increasing RAM will also improve CPU and network!

## AWS Lambda lanugage support

> Node. JS(JavaScript)

> Python

> JAVA (java 8 compatible)

> C# (. NET Core)

> Golang

> C# / Powershell

> Ruby

> Custom Runtime API (Community supported: Rust)

> Lambda Container image:

    - The container image must implement the lambda runtime API
    - ECS / Fargate is preferred for running arbitrary Docker image

## AWS Lambda Pricing:

> you can find overall pricing information here:

    https://aws.amazon.com/lambda/pricing/

> Pay per calls:

    - first 1000000 requests are free
    - $0.20 per 1 million requests therafter ($0.0000002 per request)

> Pay per duration: (in increment of 1 MS)

    - 400000 GB-seconds of computer time per month if free
    - == 400000 seconds if function is 1GB RAM
    - == 3200000 seconds if function is 128 MB RAM
    - After that $1.00 for 600000 GB-seconds

> it is usually very cheapp to run aws Lambda so it's very popular

# Amazon API Gateway:

> Fully managed service for developers to easily create publish, maintain, monitor and secure API's

> Serverless and scalable

> Supports RESTful API's and WebSocket API's

> Support for security, user, authentication throttling, API keys, monitoring

# AWS Batch:

> Fully Managed batch processing at any scale

> Efficiently run 100000s of computing batch jobs on AWS

> A "Batch" job is a job whith a start and an end..

> Batch will dynamically launch EC2 instances or SPOT instances

> AWS Batch provisions the right amount of compute / memory

> you submit or schedule batch jobs and aws batch does the rest!!

> Batch jobs are defined as Docker images and run on ECS

> Helpful for cost optimization and focusing less on the infrastructure

# Batch vs Lambda:

> Lambda:

    - Time Limit (15 minutes)
    - Limited runtimes
    - Limited temporary disk space
    - Serverless

> Batch:

    - No Time Limit
    - Any runtime as ling as it's packaged as a docker image
    - Rely on EBS / instance store for disk space
    - Replies on EC2(can be managed by AWS)
# Amazon Lightsail:

> Virtual servers, storage, databases and networking

> Low and predictable pricing

> Simpler alternative to using EC2, RDS, ELB, EBS, Route53..

> Great for people with little cloud experience

> Can setup notifications and monitoring of your lightsail resources

> Use cases:

    - simple web applications(has templates for LAMP,Nginx,Mean,NodeJS...)
    - Websites(templates for WordPress,Magento,Plesk,joomla)

> Has high availablity but not auto-scaling, limited AWS integrations

<!-- CloudFormation -->

> CloudFormation is a declarative way of outlining your aws infrastructure, for any resources (most of them are supported )

> for example, within a CloudFormation template, you say:

    - i want a security group
    - i want two ec2 instances using this security group
    - i want as s3 bucket
    - i want a load balancer(ELB) in front of these machines

> then CloudFormation creates those for you, in the right order with the exact configuration you specify

> Benefits of AWS CloudFormation :

* Infrastructure as code (IAC)

  + no resources are manually created which is excellent for control
  + Changes to the infrastructure are reviewed through code

* Cost:

  + Each resource within the stack is tagged with an identifire so you can easily see how much a stack costs you
  + you can estimate the costs of your resiurces using the CloudForamtion template
  + Saving Strategy: in dev, you could automation deletion of templates at 5 pm and recreated at 8 am, safely

* Productivity:

  + Ablity to destory and re-create an infrastructure on the cloud on the fly
  + Automated generation of diagram for your templates
  + Declarative programming (no need to figure out ordering and orchestration)

* don't re-invent the wheel:
  + leverage existing templates on the web
  + leverage the documentation

<!-- sample yaml code for Iac -->

> ec2.yaml

Resources:
MyInstance:
Type: AWS:: EC2:: Instace
AvaliblityZone: us-east-1a
ImageId: ami-a4c7edb2
InstanceType: t2.micro

> ec2-with-sg.yaml

Parameters:
SecurityGroupDescription:
Description: Security Group Descripton
Type: String

Resources:
MyInstance:
Type: AWS:: EC2:: Instance
Properties:
Availblityzone: us-east-1a
ImageId: ami-a4c7edb2
InstanceType: t2.micro
SecurityGroups: - ! Ref SSHSecurityGroup - ! Ref ServerSecurityGroup

<!-- # an elastic ip for our instance -->

MyIP:
Type: AWS:: EC2:: EIP
Properties:
InstanceId: ! Ref MyInstance

<!-- # our EC2 Security Group -->

SSHSecurityGroup:
Type: AWS:: EC2:: SecurityGroup
Properties:
GroupDescription: Enable SSH Access via port 22
SecurityGroupIngress: - CidrIP: 0.0.0.0/0
FromPort: 22
InProtocol: tcp
ToPort: 22

<!-- # Our second EC2 security group -->

ServerSecurityGroup:
Type: AWS:: EC2:: SecurityGroup
Properties:
GroupDescription: ! Ref SecurityGroupDescription
SecurityGroupIngress: - IpProtocol: tcp
FromPort: 80
ToPort: 80
CidrIP: 0.0.0.0/0 - IpProtocol: tcp
FromPort: 22
ToPort: 22
CidrIP: 192.168.1.1/32

Outputs:
ElasticIP:
Description: Elastic IP Value
Value: ! Ref MyEIP

<!-- AWS Cloud Development Kit (CDK) -->

# AWS Cloud Development Kit (CDK):

> Define your Cloud Infrastructure using a familiar language

> JS/TypeScript, Python, Java, . NET...

> this code is compiled into CloudFormation template (JSON/YAML)

> you can therefore deploy infrastructure and application runtime code together

    - Great for Lambda functions
    - Create for Docker containers in ECS/EKS

> Using CDK CLI -> Generates CloudFormation Template -> CloudFormation

<!-- CDK Code Example -->

export class MyECSConstructStack extends core. Stack{
constructor(scope: core, App, id: String, props ?: core. StackProps)
super(scope, id, props); 

    const vpc = new ecc2.Vpc(this, "MyVpc",{
        maxAZs: 3 // Default is all AZs in region
    });

    const cluster = new ecs.Cluster(this,"MyCluster",{
        vpc:vpc
    });

    new ecs_pattern.ApplicationLoadBalancedFargetService(this,"Myservice",{
        cluster: cluster, //Required
        cpu:512, // default is 256
        desiredCount: 6, // default is 1
        taskImageOptions: {
            image: ecs.ContainerImage.fromRegistry("AWS::Registry")
        },
        memoryLimitMiB: 2048, // default is 512
        publicloadBalancer: true // default is false
    });

}

<!-- Beanstalk -->

> Developers problems on aws:

* Managing infrastructure

* Deploying code

* configuring all the databases and load balancers etc...

* Scaling concerns

* most web apps have the same architecture(ALB + ASG)

> Elastic Beanstalk is a developer centric view of deploying an application on aws

> it uses all the component's (EC2, ASG, ELB, RDS, etc...)

> we still have full control over the configuration

> BeanStalk = Platform as a Service (PaaS)

> Beanstalk is free only pay for underlying services

> Managed Service:

    - Instannce configuration/OS is handled by beanstalk
    - Deployment strategy is configurable but performed by Elastic Beanstalk
    - Capacity provisioning
    - Load balancing and autoscaling
    - Application health-monitoring and responsiveness

> Just the application code is the responsiblity of the developer

# 3 Architecture models of Elastic BeanStalk:

> Single instance deployement: good for dev

> LB + ASG: great for production and pre-prod web apps

> ASG only: great for non web apps in productions

# Elastic Beanstalk supports platforms

> Go, JAVA SE, Java with tomcat
> . NET on windows Server with IIS
> Node.js, PHP, Python, Ruby, Packer Builder
> Single Container Docker
> Multi-Container Docker
> PreConfigured Docker

> If not supported you can write your custom platforms

## Elastic Beanstalk - Health Monitoring

> Health agent pushes metrics to CloudWatch
> Checks for app health, publishes health events

> it uses CloudFormation in background to cretae the services

# AWS CodeDeploy

> We want to deploy our application automatically

> Works with EC2 instances
> Works witn On-premises Servers
> Hybrid Service
> Servers/Instances must be provisioned and configured ahead of time with the CodeDeploy Agent

# Code Commit

> Before Pushing the application code to servers, it needs to be stored somewhere

> Developers usually stores code in a repository, using Git technology

> A famous public offering is GitHub, AWS competing product is CodeCommit

> CodeCommit:

    - Source-control service that hosts git-based repo's
    - Makes it easy to collaborate with others on code
    - the code changes are automatically versioned

> Benefits:

    - Fully Managed
    - Scalable and highly available
    - Private,Secured integrated with AWS.

# Code Build:

> AWS Code Build is the code building service in the cloud

> Compilers source code, run tests and produces packages that are ready to be deployed (by CodeDeploy for ex:)

> Benefits:

    - Fully Managed Serverless
    - Continuously scalable and highly available
    - Secure
    - Pay-as-you-go-pricing - only pay for the build time

# AWS CodePipeline:

> Orchestarte the different steps to have the code automatically pushed to production

> Code ==> Build ==> Test ==> Provision ==> Deploy

> Basis for CICD(Continuous integration and Continuous Delivery)

> Benefits:

    - Fully Managed
    - Compatible with CodeCommit,CodeBuild,CodeDeploy,Elastic Beanstalk, CloudFormation,Github, 3rd-party services and custom plugins
    - Fast Delivery and rapid updates
# AWS CodeArtifacts

> Software packages depends on each other to be built (also called depencencies), and new onces are created

> Storing and retrieving these dependencies is called artifact management

> Treditionally you need to setup your own artifact management system

> CodeArtifact is a secure, scalable and cost-effective artifact management for software developement

> Works with common dependency management tools such as Maven, Gradle, NPM, Yarn, Twine, PIP, and NuGet

> Developers and CodeBuild can then retrive dependencies straight from CodeArtifacts

# AWS CodeStar

> Unified UI to easily manage software development activities in one place

> "Quick way" to get started to correctly set-up CodeCommit, CodePipeline, Codebuild, CodeDeploy, Elastic Beanstalk, EC2 etc...

> Can edit the code "in-the-cloud" using aws cloud9

# AWS Cloud9

> AWS Cloud9 is a cloud IDE (Integrated Development Environment) for writting, running and debugging code

> A cloud IDE can be used within a web browser meaning you can work on your projects from your office, home or anywhere with internet with no setup necessary

> AWS Cloud9 also allows for code collaboration in real-time(Pair-Programming)

# AWS System Manager (SSM)

> Helps to manage your ec2 and on-Premises systems at scale

> Another Hybrid AWS Service

> Get operational insights about the state of your infrastructure

> Suit of 10+ products

> Most important features are:

    - Patching automation for enhanced compliance
    - Run commands across an entire fleet of servers
    - Store Paramenter configuration with SSM Paramenter store

> Works on Linux, Windows, MacOs and Raspberry PI OS

## How System Manager works(SSM)

> We need to install the SSM agent onto the systems we control

> installed by default on Amazon Linux AMI and some ubuntu AMI

> if an instance can't be controlled with SSM, it's probably an issue with the SSM Agent

> Thanks to the SSM agent, we can run commands, path and configure our servers

## SSM Session Manager (System Manager)

> Allows you to start Secure Shell on your EC2 and on-premises servers

> No SSH access, bastion hosts or SSH keys needed

> No port 22 needed (better security)

> Supports Linux, MacOS and windows

> Send session log data to S3 or CloudWatch logs

## Systems Manager Parameter Store (SSM)

> Secure storage for configuration and secrets

> API keys, password, configurations..

> Serverless, scalable, durable, easy SDK

> Control access permissions uisng IAM

> Version tracking and encryption(optional)

# AWS OpsWorks

> Chef and Puppet help you perform server configuration automatically or repetitive actions

> they work great with EC2 and on-premises VM

> AWS OpsWorks = Managed Chef and Puppet

> it's an alternative to AWS SSM

> Only provision standard AWS resources:

    - Ec2 instances,Databases,Load Balancers,EBS volumes..
# Deployment Summary:

> CloudFormation: (AWS only)

    - Infrastructure as code(IAC),works with almost all of aws resources
    - Repeat across regions and accounts

> AWS BeanStalk: (AWS only)

    - Platform as a Service(Paas),limited to certain programming languages or docker
    - Deploy code consistently with known architecture: ex: ALB+EC2+RDS

> CodeDeploy: (hybrid)

    - deploy and upgrade any application onto servers

> System Manager(SSM): (Hybrid)

    - Patch,configure and run commands at scale

> OpsWork: (Hybrid)

    - Managed Chef and Puppet in AWS
# Developer Services Summary:

> CodeCommit:

    - Store code in private git repository (version controlled)

> CodeBuild:

    - Build and test code in AWS

> CodeDeploy:

    Deploy code onto servers

> CodePipeline:

    Orchestration of pipeline (from code to build to deploy)

> CodeArtifacts:

    - Store software packages/dependencies on AWS

> CodeStar:

    - Unified view for allowing developers to do CICD and code

> Cloud9:

    - Cloud IDE with collab

> AWS CDK:

    - Define your Cloud infrastructure using a programming language

# AWS Global application

## Why make a Global Application?

> A Global application is an application deployed in multiple geographies

> on aws: this could be Regions and or Edge locations

> Decreased Latency:

    - Latency is the time it takes for a network packet to reach a server
    - It takes time for a packet from asia to reach the US
    - Deploy your application closer to your users to decrease latency, better experience

> Disaster Recovery(DR):

    - if an aws region goes down(Earthquake,storms,power shutdoen)..
    - You can fail-over to another region and have your application still working
    - A DR plan is important to increase the availablity of your application

> Attack protection:

    - distributed global infrastructure is harder to attack

-

# Global AWS Infrastructure

> Regions:

    for deploying application and infrastructure

> Availablity Zones:

    Made of multiple data centers

> Edge locations (point of presence):

    Content delivery as close as possible to users

> [More at:](https://infrastructure.aws/)

## Global applications in AWS

> Global DNS: Route 53:

    - Great to route users to the closest deployment with least latency.
    - Great for disaster recovery strategies

> Global Content Delivery Network(CDN): CloudFront:

    - Replicate part of your applications to aws edge locations - decrease latency
    - Cache common requests - improved user experience and decreased latency

> S3 Transfer Acceleration:

    - Acclerate global uploads and downloads into amazon S3

> AWS Global Accelerator:

    - improve global application availablity and performance using the AWS global network

# Amazon Route 53

> Route53 is a managed DNS (Domain Name System)

> Dns is a collection of rules and records which helps clients understand how to reach a server through URL's

> in AWS most common records are:

    - www.google.com => 12.34.56.78 == A record(IPv4)
    - www.google.com => 2001:0db8:85a3:0000:0000:8a2e:0370:7334 == AAAA record(IPv6)
    - search.google.com => www.google.com == CNAME:hostname to hostname
    - example.com => AWS resource == Alias (ex: ELB,CloudFront,S3,RDS,etc...)

## Route 53 Routing policies

> Simple Routing policy

> Weighted Routing policy

> Latency Routing policy

> Failover Routing policy

# AWS CloudFront

> Content Delivery Network(CDN)

> improves read performance, content is cached at the edge

> improves user experience

> 216 point of presence globally (Edge Locations)

> DDoS protection (because worldwide), integration with shield, AWS Web Application Firewall

## CloudFront - Origins

> S3 Bucket:

    - for distributing files and caching them at the edge
    - Enhanced security with CloudFront Origin Access Control(OAC)
    - OAC is replacing Origin Access Identity(OAI)
    - CloudFront can be used as an ingress(to upload files to S3)

> Custom Origin (HTTP):

    - Application Load Balancer
    - EC2 instance
    - S3 website (must first enable the bucket as a static S3 website )
    - Any HTTP backend you want

## CloudFront vs S3 Cross Region Replication

> CloudFront:

    - Global Edge network
    - Files are cached for a TTL (Maybe a day )
    - Great for static content that must be available everywhere

> S3 Cross Region Replication:

    - Must be setup for each region you want replication to happen
    - Files are updated in near real-time
    - Read only
    - Great for Dynamic content that needs to be available at low-latency in few regions
# S3 Transfer Acceleration

> Increase transfer speed by transferring files to an aws edge location which will forward the data to the S3 bucket in the target region

# AWS Global Accelerator

> Improve Global applicatoin availablity and performance using the aws global network

> Leverage the aws internal network to optimize the route to your application (60% improvement)

> 2 Anycast IP(Static IP) are created for your application and traffic is sent through Edge Locations

> the edge locations send the traffic to your application

## AWS Global Accelerator vs CloudFront

> they both use the aws global network and it's edge locations around the world

> both services integrate with aws shield for DDoS protection

> CloudFront:

    - improves performance for your cacheable contents (such as images and videos )
    - Content is Served at the edge

> Global Accelerator:

    - No Caching,proxy packets at the edge to application running in one or more aws regions
    - improves performance for a wide range of application over TCP or UDP
    - Good for HTTP use cases that required static ip addresses
    - Good for HTTP use cases that required deterministic, fast regional failover
# AWS Outposts

> Hybrid Cloud: business that keeps an on-premises infrastructure alongside a cloud infrastructure

> therefore, two ways of dealing with it systems:

    - one for the aws cloud (using aws console,CLI,and aws API's)
    - one for their on-premises infrastructure

> AWS Outposts: are "server racks" that offers the same aws infrastructure, services api's and tools to build your own applications on-premises just as in the cloud

> AWS will setup and manage "Outposts Racks" within your on-premises infrastructure and you can start leveraging aws services on-premises

> you are responsible for the outposts rack physical security

## Benefits of aws outposts

> Low latency access to on-premises systems

> Local data processing

> Data residency

> Easier migration from on-premises to the cloud

> Fully managed service

> Some Services that works on Outposts:

    - Amazon EC2, Amazon EBS, Amazon S3, Amazon EKS, Amazon RDS, Amazon EMR
# AWS WaveLength

> WaveLength Zones are infrastructure deployments embedded within the telecommunications providers data centers at the edge of the 5G network

> brings aws services to the edge os the 5G networks

> example: EC2, EBS, VPC..

> ultra low latency applications through 5G networks

> Traffic dosen't leave the communication service provider's (CSP) network

> High-bandwidth and secure connection to the parent AWS Region

> No additional charges or service agreements

> Use cases:

    Smart Cities, ML-assisted diagnostics, Connected vechicles, interactive live video streams, AR/VR, Real-time Gaming..

# AWS Local Zones

> Place AWS Compute, storage, database and other selected AWS Services closer to end users to run latency-sensitive applications

> Extend your VPC to more locations - "Extension of an AWS Region"

> Compatible with EC2, RDS, ECS, EBS, ElastiCache, DirectConnect...

# Global Application Architecture

> Single Region, Single AZ

    - no High availablity
    - No Global latency
    - Difficult to setup

> Single Region, Multi AZ

    - High availablity
    - No Global latency
    - difficult to setup

> Multi Region, Active-Passive

    - Global Read latency
    - No Global Write latency
    - Difficult to setup

> Multi Region, Active-Active

    - Read Latency
    - Write Latency
    - Difficult to setup
# Global Application in AWS - Summary

> Global DNS: Route53

    - Great to route users to the closest deployment with least latency
    - Great for disaster recovery strategies

> Global Content Delivery Network(CDN): CloudFront

    - Replicate part of your application to aws edge locations - decrease latency
    - Cache common request - improved user experience and decreased latency

> S3 Transfer Acceleration:

    - Acclerate global uploads and downloads into AWS S3

> AWS Global Accelerator:

    - improve global application availablity and performance using the aws global network

> AWS Outposts:

    - Deploy outposts racks in your own data centers to extend aws services

> AWS Wavelength:

    - brings aws services to the edge of the 5G networks
    - ultra low latency applications

> AWS Local Zones:

    - Bring AWS resources closer to your users
    - good for latency sensitive applications
# Cloud Integration in AWS

> when we start deploying multiple applications, they will inevitably need to communicate with one another

> There are two patterns of application communication:

    - Synchronous Communications (1v1)
    - Asynchronous/Event based Communication (1v2v3)

> Synchronous between applications can be problematic if there are sudden spikes of traffic

> What if you need to suddenly encode 1000 videos but usually it's 10?

> in that case, it's better to decouple your applications:

    - using SQS: Queue model
    - using SNS: pub/sub model
    - using Kinesis: real-time data streaming model

> These services can scale independently from our application!

# AMAZON SQS - Simple Queue Service

> Oldest AWS offering (over 10 years old)

> Fully Managed service (~Serverless), use to decouple applications

> Scales from 1 message per second to 10, 000s per second

> Default retention of messages: 4days, maximum of 14 days

> No limit to how many messages can be in the queue

> Messages are deleted after they're read by consumers

> Low Latency (<10 ms on publish and receive)

> Consumers share the work to read messages and scale horizontally

## Amazon SQS - FIFO Queue

> FIFO - First in First Out (ordering of messages in the queue)

> Messages are processed in order by the consumer

# Amazon Kinesis

> for the exam: Kinesis = real-time big data streaming

> Managed service to collect, process and analyze real-time streaming data at any scale

> Kinesis Data Streams:

    - Low latency streaming to ingest data at scale from hundreds of thousands of sources

> Kinesis Data Firehouse:

    - Load stream into S3, Redshift, ElasticSearch,etc..

> Kinesis Data Analysis:

    - perform real-time analytics on streams using SQL

> Kinesis Video Streams:

    - monitor real-time video streams for analytics or ML
# Amazon SNS (Simple Notification Service)

> What if you want to send one message to many receivers?

> The "Event Publishers" only sends message to one SNS topic

> As many "Event Subscribers" as we want to listen to SNS topic notifications

> each subscriber to the topic will get all the messages

> up to 12, 500, 000 subscriptions per topic, 100, 000 topic limit

> SNS --> SQS, Lambda, Kinesis data Firehouse, Emails, SMS and notifications, HTTP(s) endpoints...

# Amazon Mq

> SQS, SNS are "Cloud Native" services: Proprietary protocols from aws

> Traditional applications running from on-premises may use open protocols such as: MQTT, AMQP, STOMP, Openwire, WSS

> Amazon MQ is a managed message broker service for:

    - RabbitMQ, ActiveMQ

> Amazon MQ dosen't "scale" as much as SQS/SNS

> Amazon MQ runs on servers, can run in multi AZ with failover

> Amazon MQ has both queue features (~SQS) and topic features (~SNS)

> only used when doing a application migration else SQS and SNS scales better

# Cloud Integration Section - Summery

> SQS:

    - Queue service in AWS
    - Multiple producers,messages are kept upto 14 days
    - Multiple Consumers share the read and delete messages when done
    - Used to decouple applications in AWS

> SNS:

    - Notification service in AWS
    - Subscribers: Email,Lambda,SQS,HTTP,Mobile...
    - No message retention

> Kinesis:

    - Real time data streaming,presistence and analysis

> Amazon MQ:

    - Managed,message broker for ActiveMQ and RabbitMQ in the cloud(MQTT,AMQP..protocols)
# Cloud Monitoring

> Amazon CloudWatch Metrics:

    - CloudWatch provides metrics for every service in AWS
    - Metric is variable to monitor(CPU,networking,etc...)
    - Metrics have timestamps
    - can create CloudWatch dashboards of metrics

> Important Metrics:

* EC2 Instance:

  + CPU Utilization, Status Checks, Network(not ram)
  + Default matrics every 5 minutes
  + Option for detailed Monitoring: metrics every 1 min

* EBS Vloumes:

  + Disk Read/Writes

* S3 Buckets:

  + BucketSizeBytes, NumberOfObjetcs, AllRequests

* Billing:

  + Total Estimated Charges

* Service Limits:

  + How much you've been using a service API

* Custom metrics:
  + Push your own metrics
# Amazon CloudWatch Alarms

> Alarms are used to trigger notifications for any metric

> Alarms Actions:

    - Auto Scalling: Increase or decrease EC2 Instance
    - EC2 Actions: Stop,terminate,reboot or recover ec2
    - SNS notifications: Send a notification into an SNS

> Various options (Sampling, %, Max, Min, etc...)

> Can choose the period on which to evaluate an alarm

> Example: create a billing alarm on the CloudWatch Billing metric

> Alarm States: OK, INSUFFICIENT_DATA, ALARM

## Amazon CloudWatch Logs

> CloudWatch logs can collect log from:

* Elastic BeanStalk:

  + Collection of logs from application

* ECS:

  + Collection from containers

* AWS Lambda:

  + Collection from function logs

* CloudTrail based on filter

* CloudWatch log agents:

  + On EC2 machines or on-premises servers

* Route53:

  + Log DNS Queries

* Enables Real-time monitoring of logs

* Adjustable CloudWatch logs retention

## CloudWatch Logs for EC2

* By default, no logs from your EC2 instance will goto CloudWatch

* you need to run a CloudWatch agent on EC2 to push the log files you want

* Make sure IAM permission are correct

* The CloudWatch log agent can be setup on-premises too
# Amazon EventBridge

> Formerly CloudWatch Events

> Schedule: Cron jobs (Scheduled scripts)

> Event Pattern: Event rules to react to a service doing something

> Trigger Lambda Fucntions, send SQS, SNS messages..

> Default Event bus, Partner event bus, Custom event bus

> Schema Registry: Model even schema

> You can archive events (all/filter) sent to an event bus

> Ablity to replay archived events

# AWS CloudTrail

> Provides governance, compliance and audit for your aws account

> CloudTrail is enabled by default

> Get an history of events/API calls made within your aws account by:

    - console
    - SDK
    - CLI
    - AWS Service

> Can put logs from ClouTrail into CloudWatch logs or S3

> A Trail can be applied to all regions (default) or a single Region

> If a resource is deleted in AWS, investigate CloudTrail first.

# AWS X-Ray

> Debugging in production, the good old way:

    - Test locally
    - Add log statements everywhere
    - Re-deploy in production

> Log formats differ across applications and log analysis is hard.

> Debugging: one big monolith "easy", distributed services "hard"

> To solve above issues we can use AWS X-Ray

> it provides Visual Analysis of our applications

> Advantages of AWS X-Ray:

    - Troubleshooting performance(bottlenecks)
    - understand dependencies in a mircoservice architecture
    - pinpoint service issues
    - Review request behaviour
    - Find errors and exceptions
    - Are we meeting time SLA
    - where i am throttled?
    - identify users that are impacted
# AWS CodeGuru

> An ML-powered service for automated code reviews and application performance recommendations

> Provides two functionalities:

    - CodeGuru Reviewer: Automated code review for static code analysis(development)

    - CodeGuru Profiler: Visiblity/recommendations about application performance during runtime(production)

> CodeGuru Reviewer:

    - identify critical issues,security vulnerablities and hard to find bugs

    - Example: Common coding best practices,resource leaks,security detection,input validation

    - uses machine learning and automated reasoning

    - Hard-learned lessons across millions of code reviews on 1000s of open-source and amazon repo's

    - Supported java and python

    - integrates with GitHub,Bitbucket and AWS CodeCommit

> CodeGuru Profiler:

    - Helps understand the runtime behaviour of your application

    - Example: identify if your application is consuming excessive CPU capacity on a logging routine

> Features:

    - identify and remove code inefficiencies

    - improve application performance

    - Decrease compute costs

    - provides heap summary (identify which object using up memory)

    - Anomaly Detection

    - Supported application running on AWS or on-premises

    - Minimal overhead on application
# AWS Health Dashboard

> AWS Health Dashboard - Service History:

    - Shows all regions, all services health

    - shows historical information for each day

    - Has an RSS feed you can subscribe to

    - Previously called AWS Service Health Dashboard

> AWS Health Dashboard - Your Account:

    - Previously called AWS Personal Health Dashboard(PHD)

    - AWS Account Health Dashboard provides alerts and remediation guidance when aws is experiencing events that may impact you

    - While the service health dashboard displayes the general status of aws services, account health dashboard gives you a personalized view into the performance and availablity of the aws services underlying your aws resources

    - the dashboard displays relevant and timely information to help you manage events in progress and provides proactive notification to help you plan for scheduled activities.

    - Can aggregate data from an entire AWS organization

    - it's a global service

    - Shows how aws outages directly impact you and your aws resources

    - Alerts,remediation,proactive,scheduled activities
# Cloud Monitoring Summary

> CloudWatch:

    - Metrics: monitor the performance of aws services and billing metrics
    - Alarms: automate notification,perform EC2 action,notify to SNS based on metric
    - Logs: collect log files from ec2 instances,server,lambda functions...
    - Events(or eventBridge): react to events in aws,or trigger a rule on a schedule

> CloudTrail:

    - Audit API calls made within your AWS Account

> CloudTrail Insights:

    - Automated analysis of your CloudTrail events

> X-Ray:

    - trace requests made through your distributed applications

> AWS Health Dashboard:

    - Status of all aws services across all regions

> AWS Account Health Dashboard:

    - AWS events that impace your infrastructure

> Amazon CodeGuru:

    - automated code reviews and application performance recommendations
# VPC - Virtual Private Cloud

> Classless inter domain routing (CIDR):

> 0.0.0.0/0 --> all ip's allowed

base ipv-> 10.10.0.0
subnet mask -> 10.10.0.0/32

/32 is the magic number --> /32 means 1 ip (2^0)

/31 means 32-31=1 --> 2 ip (2^1)

/30 means 32-30=2 --> 4 ip (2^2)

/28 means 32-28 --> 16 ip (2^4) (2*2*2\*2)

/24 means 32-24 --> ip (2^8) (2*2*2*2*2*2*2\*2)

### basic CIDR

> /32 - No ip chnage
> /24 - Last ip number changes
> /16 - last 2 ip chnages
> /8 - last 3 ip chnages
> /0 - all ip values can change

> https://ipaddressguide.com/cidr

> substract 5 ip from the total count because 5 hosts are used by the amazone for the router and other configuration

## VPC - Crash Course

> IP Address in AWS:

    - IPV4 - internet protocol version 4 (4.3 billion addresses)

    - Public IPV4 - can be used on the internet

    - EC2 instance gets a new public IP address every time you stop then start it (default)

    - Private IPV4 - can be used on private networks (LAN) such as internal AWS networking(eg:192.168.1.1)

    - Private IPV4 is fixed for EC2 instances even if you start/stop them

> Elastic IP:

    - allows you to attatch a fixed public IPV4 address to EC2 Instance

    - has ongoing cost if not attatched to EC2 instance or if the EC2 instance is stopped

> IPV6 - internet protocol version 6(3.4x10^38 addresses)

    - every ip address is public (No private range)
    - example:2001:db:3333:4444:cccc:dddd:eeee:ffff

> VPC and subnets:

    - VPC: Virtual Private cloud: private network to deploy your resources (Regional resources)

    - Subnets: Allow you to partition your network inside your VPC (Availablity Zone resource)

    - A public subnet is a subnet that is accessible from the internet

    - A private subnet is a subnet that is not accessible from the network

    - To define acccess to internet and between subnet we use Route Table

> Internet Gateway and NAT Gatewayes:

    - Internet Gateway:
        * helps our VPC instances connect with the internet

    - Public subnets have a route to the internet gateways

    - Nat Gateways:
        * AWS Managed and NAT Instances allow your instances in your private subnets to access the internet while remaining private

> Network ACL(Access control list) and security groups:

    - NACL (Network ACL):
        * A firewall which controls traffic from and to subnets

        * can allow and deny rules

        * are attached at the subnet level

        * Rules only include IP Addresses

    - Security Groups:
        * A Firewall that controls traffic to and from an ENI/ an EC2 instance

        * Can have only Allow rules

        * Rules include IP Addresses and other security groups

> Network ACL's Vs Security Groups

* Security Groups:

  + Operates at the instance level

  + Supports allow rules only

  + is stateful: Retuen traffi is automatically allowed, regardless of any rules

  + we evaluate all rules before deciding whether to allow traffic

  + Applies to an instance only if someone specifies the security group when launching the instance, or associates the security group with the instance later on

* Networ ACL:

  + Operates at the subnet level

  + Supports allow rules and deny rules

  + is stateless: Retuen traffic must be explicitly allowed by rules

  + we process rules in number order when deciding whether to allow traffic

  + Automaically applies to all instances in the subnet's it's associated with.

> https://docs.aws.amazon.com/vpc/latest/userguide/VPCSecureity.html#VPCSecurityComparison

> VPC Flow Logs:

    - Capture nformation about IP traffic going into your interfaces:
        * VPC Flow Logs
        * Subnet Flow Logs
        * Elastic Network Interface Flow Logs

    - Helps to monitor and troubleshoot connectivity issues.Example:
        * Subnet to internet
        * Subnets to Subnets
        * Internet to Subnets

    - Captures network information from aws managed interfaces too:
        * Elastic Load Balancers
        * ElastiCache
        * RDS
        * Aurora, ETC...

    - VPC Flow logs data can go to S3,CloudWatch logs,and Kinesis Data Firehouse

> VPC Peering:

    - Connect two VPC,privately using AWS network

    - Make them behave as if they were in the same network

    - Must not have overlapping CIDR (IP Address Range)

    - VPC Peering connection is not transitive (Must be established for each VPC that need to communicate with one another)

> VPC Endpoints:

    - Endpoints allow you to connect AWS Services using a private network instead of the public www network

    - This gives you enhanced security and lower latency to access AWS Services

    - VPC Endpoint Gateway:
        * S3 and Dynamo DB

    - VPC Endpoint Interface: The rest

> AWS PrivateLink (VPC Endpoint Services):

    - Most secure and scalable way to expose a service to 1000s of VPC's

    - Does not require VPC Peering,internet gateway,NAT,route tables...

    - Requires a network load balancer (Service VPC) and ENI (Customer VPC) (Elastic network interface )

> Direct Connect/Site to Site VPN:

    - Site to Site VPN:
        * Connect an on-premises VPN to AWS
        * The Connection is automatically encrypted
        * Goes over the public internet
        * Can be setup very quickly
        * On-premises must use a Customer Gateway (CGW)
        * AWS Must use a Virtual Private Gateway (VGW)

    - Direct Connect (DX):
        * Establish a physical connection between on-premises and AWS
        * The connection is private,secure and fast
        * Goes over a private network
        * Takes at least a month to establish

> AWS Client VPN:

    - Connect from your computer using OpenVPN to your private network in AWS and on-premises

    - Allow you to connect to your EC2 instances over a private IP

> Transit Gateway:

    - For having transitive peering between thousands of VPC and on-premises,hub-and-spoke(star) connections

    - one single gateway to provide this functionality

    - Works with Direct Connect Gateway, VPN Connections
# VPC Networking Summary

> VPC : Virtual Private Cloud

> Subnets: Tied to an AZ, Network partition of the VPC

> Internet Gateway: at the VPC level, provides internet access

> NAT Gateway/Instances: Give internet access to private subnets

> NACL: Stateless, subnet rules for inbound and outbound

> Security Groups: Stateful, operates at the EC2 instance level or ENI

> VPC Peering: Connect two VPC with non overlapping IP Ranges, nontransitive

> Elastic IP: Fixed public IPV4, ongoing cost if not in use

> VPC Endpoints: provide private access to AWS services within VPC

> PrivateLink: Privately connect to a service in a 3rd party VPC

> VPC Flow Logs: Network traffic logs

> Site to Site VPN: VPN over public internet between on-premises direct connect and AWS

> Client VPN: OpenVPN connection from your computer into your VPC

> Direct Connect: direct private connection to AWS

> Transit Gateway: Connect thousands of VPC and on-premises networks together

https://aws.amazon.com/architecture/icons/

# AWS Shared Responsibility Model

> AWS Responsiblity - Security of the cloud

    - Protecting infrastructure that runs all the aws services
    - Managed services like S3,DynamoDB,RDS ETC...

> Customer Responsiblity - Security in Cloud

    - for EC2 instance,customer is responsible for management of the guest OS,firewall and network configuration,IAM
    - Encrypting application data

> Shared Controls

    - Path Management,Configuration management, Awareness and Training
## Example: RDS Responsiblity:

> AWS:

    - Manage the underlying EC2 Instance,disable SSH Access
    - Automated DB Patching
    - Automated OS Patching
    - Audit the underlying instance and disk and gurantee it functions

> Customer:

    - Check the ports / IP / security Group inbound rules in DB's Security groups
    - in-database user creation and permission
    - Creating a database with or without public access
    - Ensure Parameter groups or DB is confifured to only allow SSL Connections.
    - Database encryption settings
## Example: S3

> AWS:

    - Guarantee you get unlimited storage
    - Guarantee you get encryption
    - Ensure sepration of the data between different customers
    - Ensure AWS employees can't access your data

> Customer:

    - Bucket configuration
    - Bucket policy / public setting
    - IAM user and roles
    - Enabling encryption

> Visit this link for more - <b><u>[responsiblity_model](https://aws.amazon.com/compliance/shared-responsiblity-model/) </u></b>

# WAF and DDoS Attack protection

> AWS Shield standard:

    - protects against DDoS Attack for your website and applications, for all customers at no additional costs
    - provides protection from attatcks such as SYN/UDP floods,reflection attacks and other layer 3/4 attacks

> AWS Shield Advanced:

    - 24/7 premium DDoS protection
    - Optional DDoS mitigation service ($3000 per month per organization)
    - Protects against more sophisticated attack on Amazon EC2,Elasti Load Balancing, Amazon CloudFront, AWS Global Accelerator and Route53
    - protects against higher fees during usage spikes due to DDoS

> AWS WAF: Filter specific requests based on rules

> CloudFront and Route53:

    - Availablity protection using global edge network
    - Combined with AWS Shield providdes attatck mitigation at the edge

> Be ready to Scale: Leverage AWS Auto Scaling

> Sample reference <b><u>[DDOS Protection](https://aws.amazon.com/answers/networking/aws-ddos-attack-mitigation/)</u></b>

# AWS WAF (Web Application Firewall)

> Protects your web applications from common web exploites (Layer 7)

> Layer7 is HTTP (vs Layer 4 is TCP)

* Deploy on application load balancer, API gateway, cloudFront

> Define web ACL (Access Control List)

* Rules can include IP Addresses, HTTP Headers, HTTP body or URL strings
* Protects from common attack - SQL injection and Cross-Site-Scripting (xss)
* Size constraints: geo-match (block countries)
# AWS Network Firewall

> Protect your entire Amazon VPC

> From layer 3 to layer 7

> Any direction you can inspect:

    - VPC to VPC traffic
    - Outbound to internet
    - inbound to internet
    - TO and from direct connect and site to site VPN
# Encrypted data

# Data at rest vs Data in transit

> Data Rest:

    - Data stored or archived on a device
    - on a hard Disk, on a RDS instance, in S3 Glacier Deep Archive,etc..

> In Transit(in motion):

    - Data being moved fom one location to another
    - Transfer from on-premises to AWS,EC2 to DynamoDB etc
    - Means data transferred on the network

> We want to encrypt data in both states to protect it!

> For this we leverage encryption keys

# AWS KMS (Key Management Service)

> Anytime you hear "Encryption" for an AWS service, it's most likely KMS

> KMS = AWS manages the encryption keys for us

> Encryption opt-in:

    - EBS Volumes encrypt of objects
    - S3 buckets: Server-side encryption of objects
    - Redshift database: Encryption of data
    - EFS drives: Encryption of data

> Encryption Automatically Enabled:

    - CloudTrail Logs
    - S3 Glacier
    - Storage Gateway
# CloudHSM (other service to manage keys)

> KMS => AWS Manages the software for encryption

> CloudHSM => AWS provisions encryption hardware

> Dedicated hardware(HSM = Hardware security Module)

> You manage your own encryption keys entirely

> HSM device is temper resistant, FIPS 140-2 level 3 compliance

# Types of KMS Keys

> Customer Managed Key:

    - Create,manage and used by the customers,can enable or disable
    - Possibility of rotation policy
    - Possibility to bring-your-own-key
    - will cost money
    - Schedule key deletion or delete it manually

> AWS Managed Key:

    - created and managed and used on the customer's behalf by AWS
    - Used by aws services(aws/s3,aws/ebs,aws/redshift)

> AWS Owned Key:

    - Collection of CMK's that an aws service owns and manages to use in multiple accounts
    - AWS can use those to protect resources in your account(but you can't view the keys)

> CloudHSM Keys (Custom KeyStore):

    - Keys generated from own CloudHSM hardware device
    - Cryptographic operations are performed within the CloudHSM cluster
# AWS Certificate Manager (ACM)

> Let's you easily provision, manage and deploy SSL/TLS Certificates

> Used to provide in-flight encryption for websites(HTTPS)

> Supports both public and private TLS certificates

> Automatic TLS certificate renewal

> Integration with(load TLS certificates on):

    - Elastic Load Balancers
    - CloudFront Distributions
    - API's on API gateway

> AWS SECrets Manager:

    - Newer Service,Meant for storing secrets
    - Capablity to force rotation of secrets ecery x days
    - Automate generation of secrets on rotation(uses Lambda)
    - Integration with Amazon RDS (MySql,PostGreSql,Aurora)
    - Secerets are encrypted using KMS
    - Paid Service
    - Mostly meant for RDS Integration
# AWS Artifact

> Portal that provides customers with on-Demand access to aws compliance documentation and aws agreements

> Artifact Reports - Allows you to download AWS security and compilance documents from third-party auditors like AWS ISO certifications, Payment Card industry(PCI) and system and organization Control(SOC) reports

> Artifact Agreements - Allows you to review, accept and track the status of AWS Agreements such as the business Associate Addendum(BAA) or the Health Insurance Portability and Accountability ACT(HIPPA) for an individual account or in your organization

> Can be used to support internal Audit or Compliance

# AWS GuradDuty

> Intelligent Threat discovery to protect your AWS Account

> Uses Machine Learning algorithms, anomaly detection, 3rd party data

> One Click enable (30 days trial), no need to install software

> Input Data includes:

    - CloudTrail Events Logs: Unusual API calls, Unauthorized deployments

    - CloudTrail Management Events: create VPC,subnet,create trail...

    - CloudTrail S3 data events: get object,list object,delete object...

    - VPC Flow logs: Unusual internal traffic,unusual IP address

    - DNS logs: Compromised EC2 instances sending encoded data with DNS queries

    - Optional features: EKS Audit logs, RDS and Aurora, EBS,Lambda,S3 Data Events..

> Can setup EventBridge Rules to be notified in case of findings

> EventBridge rules can target AWS Lambda or SNS

> Can Protect against CryptoCurrency attack (Has a dedicated "Finding for it ")

# Amazon Inspector

> Automated Security Assessments

> For EC2 Instances:

    - Leveraging the AWS System Manager(SSM) agent
    - Analyze against unintended network accessibility
    - Analyze the running OS against Known Vulnerabilities

> For Containder Images push to Amazon ECR:

    - Assessment of container images as they are pushed

> For Lambda Functions:

    - Identifies software vulnerablities in function code and package dependencies
    - Assessment of functions as they are deployed

> reporting and integration with AWS Security Hub

> Send finding to Amazon Event Bridge

> only for EC2 instance, Container images and Lambda functions

> Continuous scanning of the infrastructure, only when needed

> Package vulnerabilities(EC2, ECR, Lambda) - Database of CVE

> Network reachablity(EC2)

> A Risk Score is associated with all vulnerablities for prioritization

# AWS Config

> Helps with auditing and recording compliance of your AWS resources

> Helps record configurations and changes over time

> possibility of storing the configuration data into s3(Analyzed by Athena)

> Questions that can be solved by AWS Config:

    - is there unrestricted SSH access to my security groups?
    - Do my bucket have any public access?
    - How has my ALB configuration changed over time?

> You can receive alerts(SNS notifications) for any changes

> AWS Config is a per-region service

> Can be aggregated across regions and accounts

> Not a free service

# Amazon Macie

> Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in aws

> Macie helps identify and alert you to sensitive data such as personally identifiable information(PII)

# AWS Security Hub

> Central Security tool to manage security across several AWS accounts and automate security checks

> Integrated dashboards showing current security and compliance status to quickly take actions

> Automatically aggregates alerts in predefined or personal findings formats from various AWS services and AWS partener tools:

    - Config
    - GuradDuty
    - Inspector
    - Macie
    - IAM Access Analyzer
    - AWS System Manager
    - AWS Firewall Manager
    - AWS Health
    - AWS Partner Netowrk Solutions

> Must first enable the AWS Config Service

# Amazon Detective

> GuardDuty, Macie and security hub are used to identify potential security issues or findings

> Sometimes security findings requires deeper analysis to isolate the root cause and take action - it's complex process

> Amazon Detective analyzes, investigates and quickly identifies the root cause of security issues or suspicious activities (using ML and Graph)

> Automatically collects and processes events from VPC Flow Logs, CloudTrail, GuardDuty and creates a unified view

> Produces visualizations with details and context to get the root cause

# AWS Abuse

> Reports suspected AWS resources used for abusive or illegal purposes

> Contact aws abuse team: <b><u>abuse@amazonaws.com</u></b>

# Root User Privileges

> Root user = Account owner(Created when the account is created)

> Has complete access to all AWS Services and resources

> Lock away your AWS account root user access keys!

> Do not use the root account for everyday tasks, even administrative tasks

> actions that can be performed only by the Root User:

    - Change account settings
    - View Certain tax invoices
    - close your aws account
    - restore IAM user permissions
    - change or cancel your aws support plans
    - register as a seller in the reserved instance marketplace
    - Configure an Amazon S3 bucket to enable MFA
    - Edit or delete an amazon S3 bucket policy that included an invalid VPC Id or VPC endpoint ID
    - sign up for GovCloud
# IAM Access Analyzer

> Find out which resources are shared externally:

    - S3 Bucket
    - IAM Roles
    - KMS Keys
    - Lambda Functions and layers
    - SQS queues
    - Secrets Manager Secrets

> Define Zone Of Trust = AWS Account or AWS Organization

> Access outside zone of trust => Findings

# Summary: Security and compliance

> Shared Responsiblity on AWS

> Shield: Automatic DDoS protection + 24/7 support for advanced

> WAF: Firewall to filter incoming requests based on rules

> KMS: Encryption Keys Managed by AWS

> CloudHSM: Hardware encryption, we manage encryption keys

> AWS Certificate Manager: Provision, manage and deploy SSL/TLS Certificates

> Artifact: Get access to compliance such as PCI, ISO, etc..

> GuardDuty: Find Malicious behaviour with VPC, DNS and cloudtrail logs

> Inspector: Find software vulnerablities in Ec2, Ecr images and Lambda Functions

> Network Firewall: Protects VPS against network attacks

> Config: Track Config changes and compliance against rules

> Macie: Find Sensitive data(ex: PII data) in amazon S3 buckets

> CloudTrail: Track API calls made by users within account

> AWS Security Hub:gather security findings from multiple AWS Accounts

> Amazon Detective: Find the root cause of security issues or suspicious activities

> AWS Abuse: Report AWS resources used for abusive or illegal purposes

> root user Privileges:

    - Change account settings
    - close your aws account
    - change or cancle your aws support plan
    - Register as a seller in the reserved instance marketplace

> IAM Access Analyzer: Identify which resources are shared externally

<!-- AWS Machine Learning  -->

# Amazon Rekognition

> Find object, people, text, scenes in images and videos using ML

> Facial analysis and facial search to do user verification, people counting

> Create a database of "familiar faces" or compare against celebritie

> Use Cases:

    - Labeling
    - Content Moderation
    - Text detection
    - Face Detection and analysis(gender,age,range,etc..)
    - Face Search and verification
    - Celebrity Recognition
    - Pathing (ex: Sports game analysis)

> <b><u>[More on](https://aws.amazon.com/rekognition)</u></b>

# Amazon Transcribe

> Automatically convert speech to text

> Uses a deep learning process called <b>Automatic Speech recognition(ASR)</b> to convert speech to text quickly and accurately

> Automatically remove Personally identifiable information (PII) using <u> <b>Redaction</b> </u>

> Supports Automatic Language identification for Multi-lingual audio

> Use Cases:

    - Transcribe customer service calls
    - automate closed captioning and subtitling
    - generate metadata for media assets to create a fully searchable archive
# Amazon Polly

> Turn text into lifelike speech using deep learning

> allowing you to create application that talk

# Amazon Translate

> Natural and accurate language translation

> Amazon Translate allows you to localize content - such as websites and applications - for international users, and to easily translate large volumes of text efficiently

# Amazon Lex and Connect

> Amazon Lex:(Same technology that powers Alexa)

> Automatic Speech Recognition(ASR) to convert speech to text

> Natural Language Understanding to recognize the intent of text, callers

> Helps build chatbots, call center bots

> Amazon Connect:

    - Recive calls,create contact flows,cloud-based virtual contact center
    - Can integrate with CRM systems or AWS
    - No upfront payments,80% cheaper than traditional contact center solutions
# Amazon Comprehend

> For Natural Language Processing - NLP

> Fully Managed and serverless service

> Uses Machine learning to find insights and relationships in text

    - Language of the text
    - Extract key phrases,places,people,brands or events
    - understand how positive or negative the text is.
    - Analyzes text using tokenization and parts of speech
    - Automatically organizes a collection of text files by topic

> Sample Use Cases:

    - Analyze Customer interactions (emails) to find what leads to positive or negative experinces
    - create and groups articles by topics that comprehend will uncover
# Amazon SageMaker

> Fully managed service for developers / data scientists to build ML models

> Typically difficult to do all the processes in one place + Provision servers

> Machine lerning process(simplified):predicting your exam score

# Amazon Forecast

> Fully managed service that uses ML to deliver highly accurate forecasts

> Example:predict the future sales of a raincoat

> 50% more accurate than looking at the data itself

> Reduce forecasting time from months to hours

> use cases:

    - Product Demand Planning
    - Financial Planning
    - Resource Planning,etc...
# Amazon Kendra

> Fully Managed <b><u> `Document Search Service` </b></u> powered by Mahcine Learning

> Extract answers from within a document(text, PDF, HTML, PowerPoint, MSWord, FAQ's...)

> Natural Language search capablities

> Learn from user interactions/feedback to promote preferred results(Incremental Learning)

> Ability to manually Fine-Tune search results(Importance od data, freshness, custom, ..)

# Amazon Personalize

> Fully Managed ML-service to build apps with real-time personalized recommendations

> Example: Personalized product recommendations/re-ranking customized direct marketing

> Example: User bought gardening tools, provide recommendations on the next one to buy

> Same technology used by Amazon.com

> Integrates into existing websites, applications, SMS, email marketing systems..

> Implement in days, not months(you don't need to build, train and deploy ML Solutions)

> Use cases:

    - Retail stores
    - Media and entertainment..
# Amazon Textract

> Automatically extract text, handwriting and data from any scanned documens using AI and ML

> Extract data from forms and tables

> Read and process any tupe of document (PDF, Images, etc..)

> Use Cases:

    - Invoices, Financial reports, etc..
    - Healthcare(Medical records, insurance claims)
    - Public Sector(tax forms, ID Documents, Passports)
# Summary - AWS Machine Learning

> Rekognition: Face detection, labeling, celebrity recognition

> Transcribe: audio to text conversion

> Polly: Text to Audio Conversion

> Lex: Build Conversational bots - chatbots

> Connect: Cloud Contact Center

> Comprehend: Natural Language Processing

> SageMaker: Machine Learning for every developer and data scientist

> Forecast: Build highly accurate forecasts

> Kendra: ML-powered search engine

> Personalize: Real-time personalized recommendations

> Textract: detect text and data in documents

<!-- Account Management, Billing and Supports -->

# AWS Organizations

> Global Service

> Allows to Manage <b>Multiple</b> AWS Accounts.

> The main account is the master account

> Cost Benefits:

    - Consolidated billing accross all accounts
    - Single payment method
    - Pricing benefits from aggregated usage
    - Pooling of resereved EC2 instances for optimal savings

> API is available to automate AWS Account Creation

> Restrict account privileges using <b>Service Control Policies</b> <u>(SCP)</u>

# Multi Account Strategies

> Create Accounts per department, per cost center, per dev/test/prod, based on regulatory restrictions(Using SCP), for better resource isolation (ex: VPC), to have seprate per-account service limits, isolated account for logging

> Multi Account vs One Account Multi VPC

> Use Tagging standards for billing putposes

> Enable CloudTrail on all accounts, send logs to central S3 account

# Service Control Policies (SCP)

> Whitelist or blacklist IAM actions

> Applied at the OU( organization unit ) or Account level

> does not apply to the master account

> SCP is applied to all the users and roles of the account, including root

> the SCP does not affect service-linked roles

    - Service-linked roles enable other AWS Services to integrate with AWS Organizations and can't be restricted by scp's

> SCP must have an explicit Allow (Does not allow anything by default)

> Use Cases:

    - Restrict access to certain services (ex: EMR uses)
    - Enforce PCI compliance by explicity disabling services
# SCP Example: Blacklisting and Whitelist Strategies

{
"Version": "2012-10-17", 
"Statement": [
{
"Sid": "AllowsAllActions", 
"Effect": "Allow", 
"Action": "*", 
"Resource": "*"
}, 
{
"Sid": "DenyDynamoDB", 
"Effect": "Deny", 
"Action": "dynamodb:*", 
"Resource": "*"
}
]
}

## Example 2

{
"Version": "2012-10-17", 
"Statement": [
{
"Effect": "Allow", 
"Action": [
"ec2:*", 
"cloudwatch:*"
], 
"Resource": "\*"
}
]
}

> <b><u> [More at](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_example-scps.html)</b></u>

# AWS Organization - Consolidated Billing

> When enabled, provides you with:

    - Comibned Usage: Combine the usage across all aws accounts in the AWS organization to share the volume pricing,Reserved instances and savings plan discounts
    - One Bill: get one bill for all AWS accounts in AWS Organization

> The Management account can turn off reserved instances discount sharing for any account in the AWS Organization including itself

# AWS Control Tower

> Easy way to setup and govern a secure and complliant <b><u>Multi-Account AWS Environment</b></u> based on best practices

> Benefits:

    - Automate the set up of your encironment in a few clicks
    - Automate ongoing policy management using guardrails
    - Detect policy voilations and remediate them
    - Monitor compilance through an interactive dashboard

> AWS Control Tower runs on top of AWS Organizations:

    - it Automatically sets AWS Organizations to organize accounts and implement scp's(Service Control Policies)
# AWS Resource Access Manager (AWS RAM)

> Share AWS resources that you own with other AWS accounts

> Share with any account or within your organization

> Avoide resource duplication!

> Supported resources include:

    - Aurora
    - VPC Subnets
    - Transit Gateway
    - Route53
    - EC2 Dedicated Hosts
    - License Manager Configurations..
# AWS Service Catalog

> Users that are new to AWS have too many options and may create stacks that are not compliant / in line with the rest of the organization

> Some users just want a quick self-service portal to launch a set of authotized products, pre-defined by admins

> includes: Virtual Machines, databases, storage options etc

# AWS Pricing Models

> AWS has 4 pricing models

### Pay as you go:

    - pay for what you use,remain agile,responsive,meet scale demands

### Save when you reserve:

    - Minimize risks,predictably manage budgets,comply with long-term requirements
    - Reservation are available for EC2 Reserved Instances,DynamoDb Reserved Capacity,ElastiCache Reserved Nodes,RDS Reserved Instances,Redshift Reserved Nodes

### Pay less by using more:

    - Volume based discounts

### Pay less as AWS Grows

### Free services and free tier in AWS

* IAM
* VPC
* Consolidated Billing
* Elastic BeanStalk
* CloudForamtion
* Auto Scaling Groups
* [More about free tier](https://aws.amazon.com/free/)
  + EC2 t2.micro instance for a year
  + S3, EBS, ELB, AWS Data transfer

### Compute Pricing - EC2

> only charged for what you use:

    - Number of instances
    - Instance Configurations:
        * Physical Capacity
        * Regions
        * OS and Software
        * Instance Type
        * Instance Size
    - ELB Running time and amount of data processed
    - Detailed Monitoring

> On-demand instances:

    - Minimum of 60s
    - pay per second(Linux/Windows) or per hour(other)

> Reserved Instances:

    - upto 75% discount compared to on-demand on hourly rate
    - 1 or 3 years commitment
    - All Upfront,partial upfront,no upfront

> Spot Instances:

    - upto 90% discount compared to on-demand on hourly rate
    - Bid for unused capacity

> Dedicated Hosts:

    - On-demand
    - Reservation for 1 year or 3 years commitment

> Savings plan as an alternative to save on sustained usage

### Compute Pricing - Lambda and ECS

> Lambda:

    - Pay per call
    - Pay per duration

> ECS:

    - EC2 launch type Model
    - No additional fees,you pay for aws resources stored and created in your application

> Fargate:

    - Fargate Launch Type Model
    - Pay for vCpu and memory resources allocated to your application in your containers

### Storage Pricing - S3

> Storage class:

    - S3 Standard
    - S3 Infrequent Access
    - S3 one-zone IA
    - S3 intelligent Tiering
    - S3 Glacier and S3 Glacier Deep Archive

> Number and size of objects:

    - Price can be tired (Based on Volume)

> Number of type of requests

> Data Transfer out of the S3 regions

> S3 Transfer Acceleration

> LifeCycle Transitions

> Similar Service:

    - EFS (Pay per use,has infrequent access & lifecycle rules)

### Storage Pricing - EBS

> Volume type (Based on performance)

> Storage Volume in Gb per month provisioned

> IOPS:

    - General Purpose SSD: Included
    - Provisioned IOPS SSD: Provisionned amount in IOPS
    - Megnetic: Number of requests

> Snapshots:

    - Added Data cost per GB per month

> Data Transfer:

    - Outbound data transfer are tiered for volume discounts
    - Inbound is free

### Database Pricing - RDS

> Per hour Billing

> Database characteristics:

    - Engine
    - Size
    - Memory class

> Purchase type:

    - On-Demand
    - Reserved Instance with required up-front

> Backup Storage:

    - there is no additional charge for backup to 100% of your total database storage for a region

> Additional Storage (Per GB per month)

> Number of input and output requests per month

> Deployement type (Storage I/O are variable):

    - Single A'z
    - Multiple A'z

> Data Transfer:

    - Outbound data transfer are tiered for volume discounts
    - inbound is free

### Content Delevery pricing - CloudFront

> Pricing is different across different geographic regions

> Aggregated for each edge locations, then applied to your bill

> Data Transfer Out (Volume discount)

> Number of HTTP/HTTPS requests

### Network Costs in AWS per GB

> Free for traffic in (inbound)

> same region/availablity zone having 2 EC2 if using private IP it's free

> same region different A'z using private IP $0.01

> same region different A'z using public/elastic IP $0.02

> Different region (inter-region) $0.02

> Use private IP instead of public IP for good savings and better network performance

> Use Same AZ for Maximum Savings

### Savings Plan Overview

> Commit a certain $ amount per hour for 1 to 3 years

> Easiest way to setup long-term commitments on AWS

> EC2 Savings Plan:

    - UP to 72% discount compared to On-Demand
    - Commit to usage of individual instance families in a region
    - regardless of AZ,size
    - all upfront,partial,no upfront

> Compute Savings Plan:

    - Up to 66% discount compared to On-demand
    - Regardless of family,region,size,os,tenancy,compute options
    - Compute options: EC2,Fargate,Lambda

> Machine Learning Savings Plan: SageMaker

> Setup from AWS Cost Explorer Console

> Estimate pricing at [<b><u>this</b></u>](https://aws.amazon.com/savingsplans/pricing/)

# AWS Compute Optimizer

> Reduse costs and improve performance by recommending optimal AWS resources for your Workloads

> Helps you choose optimal configuration and right size your workloads(over/under provisioned)

> Uses Machine learning to analyze your resources configurations and their utilization CloudWatch Metrics

> Supported resources:

    - EC2 instances
    - EC2 Auto Scaling Groups (ASG)
    - EBS Volumes
    - Lambda Functions

> Lower your costs by up to 25%

> Recommendations can be exported to S3

# Billing and Costing Tools

> Estimating Costs in the cloud:

    - Pricing Calculator

> Tracking Costs in the Cloud:

    - Billing Dashboard, Free Tier Dashboard
    - Cost Allocation Tags
    - Cost and Usage Reports
    - Cost Explorer

> Monitoring against Cost Plans:

    - Billing Alarms
    - Budgets

## AWS Pricing Calculator

> Available at [<b><u>this</b></u>](https://calculator.aws/)

> Estimate the cost for your solution architecture

> Cost Allocation Tags:

    - use cost allocation tags to track your aws costs on a detailed level

> AWS Generated tags:

    - Automatically applied to the resources you create
    - Starts with pregix aws: (eg. aws:createdBy)

> User-defined tags:

    - Defined by the user
    - Starts with prefix user:

> Tagging and resource groups:

    - Tags are used for organizing resources
    - EC2: instances,images,load balancers,security groups
    - RDS,VPC resources,Route53,IAM users etc..
    - Resources created by CloudFormation are all tagged the same way

> Free naming, common tags are:

    - Name
    - Environment
    - Team...

> Tags can be used to create Resource Groups:

    - Create,Maintain and view a collection of resources that share common tags
    - Manage these tags using the Tag Editor

## Cost and Usage Reports

> The AWS Cost and usage report contains the most comprehensive set of aws cost and usage data available, including additional metadate about aws services, pricing and reservation

> The AWS Cost and usage report lists AWS usage for each service category used by an account and it's IAM users in hourly or daily line items, as well as tags that you have activated for cost allocation purposes.

> can be integrated with Athena, RedShift or QuickSight

# Cost Explorer

> Visualize, Understand and manage your AWS Costs and usage over time

> Create Custom reports that analyze cost and usage data.

> Analyze your data at a high level

> Total cost and usage across all the accounts

> or Monthly, hourly, resource level granularity

> Choose an optimal Savings Plan

> <b><u>Forecast usage</b></u> up to 12 months based on previous usage

# Billing Alarms in CloudWatch

> Billing data metric is stored in CloudWatch

> Billing data are for overall worldwide AWS Costs

> It's for actual cost, not for projected costs

> Intended a simple alarm

# AWS Budgets

> Create and send alarms when costs exceeds the budget

> 4 types of budgets: Usage, Cost, Reservation, Savings plan

> For Reserved instances (R):

    - Track utilization
    - Supports EC2,ElastiCache,RDS,RedShift

> Up to 5 SNS notifications per budget

> Can filter by: Service, Linked Account, Tag, Purchase option, Instace type, Region, Availablity Zone, API operations, etc..

> same options as AWS Cost explorer!

> 2 Budgets are free, then $0.02/day/budget

# AWS Cost Anomaly Detection

> Continuously monitor your cost and usage using ML to detect ususual spends

> It learns your unique, historic spend patterns to detect on-time cost spike and/or continuous cost increase.

> Monitor AWS services, member accounts, cost allocation tags, or cost catagories

> Sends you the anomaly detection report with root cause analysis

> Get Notified with individual alerts or daily/weekly summary(using SNS)

# AWS Service Quotas

> Notify you when you're close to a service quota value threshold

> Create CloudWatch Alarms on the service Quotas console

> Example: Lambda concurrent executions

> Request a quota increase from AWS Service Quotas or shutdown resources before limit is reached

# AWS Trusted Advisor

> No need to install anything - high level AWS Account assessment

> Analyze your AWS Accounts and provides recommendation on 5 Categories:

    - Cost optimization
    - performace
    - security
    - Fault tolerance
    - Service limits

> Support Plans:

* Basic and Developer Support plans:

  + 7 Core checks:

  + S3 Bucket permissions
  + Security Groups - specific ports unrestricted
  + IAM use (one IAM user minimum)
  + MFA on Root account
  + EBS public Snapshots
  + RDS Public Snapshots
  + Service Limits

* Business and Enterprise Support Plans:
  + Full Checks
  + Full checks available on the 5 catagories
  + Ability to set CloudWatch alarms when reaching limits
  + <b>Programmatic access</b> using <b>AWS Support API</b>

# AWS Support Plan Pricing

## Basic Support: Free

> Customer Service and communities:

    - 24x7 access to customer service,documentation,whitepapers and support forums.

> AWS Trusted Advisor:

    - Access to 7 core trusted advisor checks and guidance to provision your resources following best practices to increase performace and improve security

> AWS Personal Health Dashboard:

    - A personalized view of the health of AWS Services and alerts when your resources are impacted

## Developer Support Plan:

> All Basic Support Plan+

> Business hours email access to cloud support associates

> Unlimited cases / 1 primary contact

> Case Severity / response times:

    - General guidance < 24 business hours
    - System impaired < 12 business hours

## Business Support Plan (24/7):

> Intended to be used if you have production workloads

> Trusted Advisor - Full set of checks + API Access

> 24x7 phone, email and chat access to cloud support engineers

> unlimited cased / unlimited contacts

> Access to infrastructure Event Management for Additional fee.

> Case Severity / response time:

    - General guidance < 24 business hours
    - System impaired < 12 business hours
    - Production System Impaired < 4 hours
    - Production System Down < 1 hours

## AWS Enterprise on-Ramp Support Plan (24/7)

> Intended to be used if you have production or business critical workloads

> All of the Business Support plan+

> Access to a pool of Technical Account Manager (TAM)

> Concierge Support Team(For billing and account best pracitices)

> Infrastructure Event Management, well-architected and operations Reviews

> Case Severity / response time:

    - General guidance < 24 business hours
    - System impaired < 12 business hours
    - Production System Impaired < 4 hours
    - Production System Down < 1 hours

    - Business-critical system down < 30 minutes

## AWS Enterprise Support Plan (24/7)

> Intended to be used if you have mission critical Workloads

> All of the business Support Plan +

> Access to designated Technical Account Manager (TAM)

> Concierge Support Team(For billing and account best pracitices)

> Infrastructure Event Management, well-architected and operations Reviews

> Case Severity / response time:

    - General guidance < 24 business hours
    - System impaired < 12 business hours
    - Production System Impaired < 4 hours
    - Production System Down < 1 hours

    - Business-critical system down < 15 minutes

# Account best Practices - Summary

> Operate Multiple Accounts using <b>Orgnizations</b>

> Use <b>SCP(Service Control Policies)</b> to restrict account power

> Easily setup multiple accounts with best-practices with <b>AWS Control Tower</b>

> Use <b>Tages and Cost Allocation Tags</b> for easy management and billing

> IAM Guidelines: MFA, Least-privilege, Password Policy, Password rotation

> Use <b>Config</b> to record all resources configurations and compliance over time

> Use <b>CloudFormation</b> to deploy stacks across accounts and regions

> Use <b>Trusted Advisor</b> to get insights, Support Plan adapted to your needs

> Send Service Logs and Access Logs to <b>S3 or CloudWatch Logs</b>

> Use <b>CloudTrail</b> to record API calls made within your account

> if your Account is Compromised: Change the root password, delete and rotate all passwords/key, contact the aws support.

> Allow users to create pre-defined stacks defined by admins using <b>AWS Service Catalog</b>

## Billing and Costing Tools - Summary

> Compute Optimizer: Recommends resources configuration to reduse cost

> Pricing Calculator: Cost of Services on AWS

> Billing Dashboard: high level overview + free tier dashboard

> Cost Allocation Tags: tag resources to create detailed reports

> Cost and usage Reports: Most comprehensive billing dataset

> Cost Explorer: View current usage and forecast usage

> Billing Alarms: in US-East-1 - track overall and per-serving billing

> Budgets: More advanced - Track usage, costs, RI(Reserved Instances) and get alerts

> Savings Plan: easy way to save based on long-term usage of AWS

> Cost Anomaly Detection: Detect unusual spends using ML

> Service Quotas: Notify you when you're close to service quota threshold

# AWS STS (Security Token Service)

> Enables you to create temporary, limited-privileges credentials to access your AWS resources

> Short-term Credentials: you Configure expiration period

> Use Cases:

    - <b>Identity Federation</b>: Manage identities in external systems,and provide them with STS tokens to access AWS Resources
    - IAM Role for cross/same account access
    - IAM Roles for Amazon EC2: Provide temporary credentials for EC2 instances to access AWS resources

# AWS Cognito

> <b>Identify for your web and moblie application users </b>

> Insted of creating them an IAM user, you create a user in <b><u>Cognito</b></u>

# Active Directory

> Found on any Windows Server with AD Domain services

> Database of objects: User Accounts, Computers, Printers, File Shares, Security Groups

> Centralized security management, create account, assign permissions

# AWS Directory Services

> AWS Managed Microsoft AD:

    - Create your own AD in AWS
    - Manage users locally,Supports MFA
    - Establish "Trust" connections with your on-premises AD

> AD Connector:

    - Directory Gateway(Proxy) to redirect to on-premises AD, Supports MFA
    - Users are Managed on the on-premises AD

> Simple AD:

    - AD-Compatible managed directory on AWS
    - Cannot be joined with on-premises AD

# AWS IAM Identity Center

> Successor to AWS Single Sign-on

> One Login (Single Sign-on) for all your:

    - AWS Accounts in AWS Organizations
    - Business Cloud applications(ex: Salesforce,etc..)
    - SAML2.0-enabled applications
    - EC2 Windows instances

> Identity Providers:

    - Built-in identity store in IAM identity center
    - 3rd party: Active Directory(AD),OneLogin,Okta...

## Advanced Identity - Summary

> IAM:

    - identity and access management inside your AWS Acount
    - for users that you trust and belong to your company

> Organizations: Manage Multiple Accounts

> Security Token Service(STS): Temporary, limited-privileges credentials to access AWS Resources

> Cognito: Create a database of users for your mobile and web applications

> Directory Services: integrate Microsoft Active Directory in AWS

> IAM Identity Center: One login for multiple aws accounts and applications

# Other AWS Services

> Amazon WorkSpace:

    - Managed Desktop as a Service(DaaS) solution to easily provision Windows or Linux Desktops
    - great to eliminate Management of on-premises VDI
    - Fast and quickly scalable to thousands of users
    - Secured data - Integrates with KMS
    - Pay-as-you-go service with monthly or hourly rates

> Amazon AppStream 2.0:

    - Desktop Application Streaming Service
    - Deliver to any computer,without acquiring,provisioning infrastructure
    - The application is delivered from within a web browser

## WorkSpace vs AppStream

> WorkSpace:

    - Fully Managed VDI and Desktop available
    - The users connect to VDI and open native or WAM Applications
    - Workspace are on-demand or always on

> AppStream:

    - Stream a desktop application to web browser(No need to connect to VDI)
    - Works with any device(That has a web browser)
    - allow to configure an instance type per application type(CPU,RAM,GPU..etc)

# AWS IoT Core

> IoT - Internet of Things

> the network of internet-connected device that are able to collect and transfer data

> AWS IoT core allows you to easily connect IoT devices to AWS Cloud

> Serverless, Secure and scalable to billions of devices and trillions of messages

> Your applications can communicate with your devices even when they aren't connected

> Integrates with lot of AWS Services(Lambda, S3, SageMaker)

> Can used to build IoT applications that gather, process, analyze and act on data

# Amazon Elastic Transcoder

> Elastic Transcoder is used to <b>convert media files stored in S3 into media files in the formats required by consumer playback devices</b> (phone etc...)

> Benefits:

    - Easy to Use
    - Highly Scalable: can handle large volumes of media and large file sizes
    - Cost effective: duration-based pricing model
    - Fully managed and secure,pay for what you use

# AWS AppSync

> Store and Sync data across mobile and web apps in real-time

> Makes use of <b>GraphQL</b> (Mobile technology from <b> Facebook </b>)

> Client Code can be generated automatically

> Integrations with DynamoDB / Lambda

> Real-Time Subscriptions

> Offline data synchronization (replace Cognito Sync)

> fine Grained Security

> AWS Amplify can leverage AWS AppSync in the background!

# AWS Amplify

> Set of tools and services that helps you develop and deploy scalable full stack web and mobile applications

> Authentication, Storage, API(REST, GraphQL), CI/CD, PubSub, Analyrics, AI/ML predections, Monitoring, Source Code from AWS, Github etc...

# AWS Device Farm

> Fully managed Service that tests your web and mobile apps against desktop browsers, real mobile devices and tablets

> run tests concurrently on multple devices (Speed up execution)

> Ability to configure devices settings(GPS, Wi-FI, etc...)

# AWS Backup

> Fully-Managed service to centrally manage and automate backups across aws services

> On-demand and Scheduled backups

> Supports PITR(Point in time recovery)

> Retention Periods, LifeCycle Management, Backup policies..

> Cross Region Backup

> Cross-Account Backup (using AWS Organizations)

## Disaster Recovery Strategies

> Backup and Restore:

    - Cheapest to use for backup
    - copies data from server to S3 and runs only restore to oher region and keeps application running

> Pilot Light:

    - Core Functions of the app
    - Ready to scale but minimal setup
    - cost is higher compared to <b>backup & restore</b>

> Warm Standby:

    - Full version of the app
    - at a minimum size
    - Cost is higher compared to <b>Pilot Light</b>

> Multi-Site/Hot-Site:

    - Full version of app
    - at a full size
    - Maximum amount of cost

## AWS Elastic Disaster Recovery (DRS)

> Used to be named "CloudEndure Disaster Recovery"

> Quickly and easily recover your physical, virtual and cloud-based servers into aws

> Example: protect your most critical databases (including Oracle, MySQL and SQL Serve), enterprise apps(SAP), protect your data from ransomware attacks..

> Continuous block-level replication for your servers

> adds the block level replication into AWS staging area

> in case of failover quickly deploys to production

> after on-premises/corporate server is up cna do a failback

## AWS DataSync

> Move large amount of data from on-premises to AWS

> Can synchronize to Amazon S3(any storage class - including Glacier), Amazon EFS, Amazon FSx for Windows

> Replication tasks can be scheduled hourly, daily, weekly

> The replication tasks are <b><u>incremental</b></u> after the first full load

## AWS Application Discovery Service

> plan migration projects by gathering information about on-premises data centers

> Server utilization data and dependency mapping are important for migrations

> Agentless Discovery(AWS Agentless Discovery Connector):

    - VM inventory,Configuration and performace history such as CPU,Memory and disk usage

> Agent-based Discovery(AWS Application Discovery Agent):

    - System configuration,system performance,running processes and details of the network connections between systems

> above resulting data can be viewed within AWS Migration Hub

## AWS Application Migration Service (MGN)

> The "AWS evolution" of CloudEndure Migration, replacing AWS server migration Service(SMS)

> Lift-and-shift(Rehost) solution which simplify migrating applications to AWS

> Converts your physical, virtual and cloud-based servers to run natively on AWS

> in corporate Data Centers/Any Cloud the AWS Replication Agent will run Continous Replication to AWS cloud on low-cost EC2 instances and EBS volumes

> once application is ready on the day of cutover the instances and data will be copied to prod

> Supports wide range of platforms, operating systems and databases

> Minimal downtime, redused costs

## AWS Migration Evaluator

> Helps you build a data-driven business case for migration to AWS

> Provides a clear baseline of what your organization is running today

> Install Agentless collector to conduct broad-based discovery

> Take a snapshot of on-premises foot-print, server dependencies..

> Analyze current state, define target state then develop migration plan

## AWS Migration Hub

> Central location to collect servers and applications inventory data for the assessment planning, and tracking of migration to aws

> Helps accelerate your migration to AWS, automate lift-and-shift

> AWS Migration Hub Orchestrator - Provides pre-built templates to save time and effort migrating enterprise apps (e.g: SAP, Microsoft SQL Server...)

> Supports migration status uodates from application migration service (MGN) and database migration Service (DMS)

## AWS Fault injection Simulator (FIS)

> A fully Managed Service for running fault injection experiments on AWS Workloads

> Based on Chaos Engineering - Stressing an application by creating disruptive events, observing how the system responds and impplementing improvements

> Helps you uncover hidden bugs and performance bottlenecks

> Supports the following AWS Services: EC2, ECS, EKS, RDS...

> Use Pre-built templates that generate the desired disruptions

# Step Functions

> Build Serverless visual workflow to orchestate your <b>lambda fuctions</b>

> Features:

    - Sequence
    - Parallel
    - Conditions
    - Timeouts
    - Error Handling ...

> Can integrate with EC2, ECS, on-premises servers, API Gateway, SQS Queues etc...

> Possibility of implementing human approval feature

> Use Cases:

    - Order Fulfillment
    - Data Processing
    - Web Applications
    - Any Workflow..

# AWS Ground Station

> Fully Managed Service that let's you <b>control satellite communications, process data and scale your satellite operations</b>

> Provides a global network of satellite ground stations near AWS Regions

> Allows you to download satellite data to your AWS VPC within seconds

> Send Satellite data to S3 or EC2 instance

> Use Cases:

    - Weather Forecasting
    - Surface Imaging
    - Communications
    - Video Broadcasts

# Amazon Pinpoint

> Scalable 2-way (outbound/inbound) marketing communications service

> Supports Email, SMS, Push, Voice and in-app messaging

> Abillity to segment and personalize messages with the right content to customers

> Possibility to receive replies

> Scales to Villions of messages per day

> Use Cases:

    - Run Campaigns by sending marketing
    - Bulk
    - Transactional SMS Messages

> SNS VS SES VS Pinpoint

    - in SNS and SES you managed each message's auidence, content and delivery schedule

    - In Pinpoint you create message templates,delivery schedules,highly-targeted segments and full campaigns

# AWS Architecting & Eco-system

> `Well Architected Framework General Guiding Principles`

> Stop guessing your capacity needs

> Test systems at production scale

> Automate to make architectural expermentation easier

> Allow for evolutionary architectures:

    - Design based on changing requirements

> Drive architectures using data

> Improve through game days:

    - Simulate applications for flash sale days

## AWS Cloud Best Practices - Design Principles

> Scalability: Vertical and Horizontal

> Disposable Resources: Servers should be disposable and easily configured

> Automation: Serverless, Infrastructure as a service, Auto Scalling...

> Loose Coupling:

    - Monolith are applications that do more and more over time,become bigger
    - Break it down into smaller,loosely couples components
    - A change or a failure in one component should not cascade to other components

> Services, not servers:

    - Don't use just EC2
    - Use Managed Services,databases,serverless etc..

## Well Architected Framework 6 Pillars

> 1. Operational Excellence
> 2. Security
> 3. Reliablity
> 4. Performance Efficiency
> 5. Cost Optimization
> 6. Sustainablity

### 1. Operational Excellence

> Include the ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures

> Design Principles:

    - Perform operations as code - Infrastructure as code
    - Annotate documentaion - Automate the creation of annotated documentaion after every build
    - Make frequent,small,reversible changes - so that in case of any failure you can reverse it
    - Refine operations procedures frequently - and ensure that team members are familiar with it
    - Anticipate failures
    - Learn from all operational failures

> > Operational Excellence AWS Services

> Prepare:

* AWS CloudFormation
* AWS Config

> Operate:

    - AWS CloudFormation

    - AWS Config

    - AWS CloudTrail

    - Amazon CloudWatch

    - AWS X-ray

> Evolve:

    - AWS CloudFormation

    - AWS CodeBuild

    - AWS CodeCommit

    - AWS CodeDeploy

    - AWS CodePipeline

### 2. Security

> Includes the ability to protect information, systems and assets while delivering business value through risk assessments and mitigation strategies

> Design Principles:

    - Implement a strong identity foundation: centralize privilge management and reduce reliance on lon-term credentials

    - Principle of least privilege: IAM

    - enable traceablity: integrate logs and metrics with systems to automatically respond and take actions

    - Apply security at all layers: Like edge network,VPC,Subnet,load balancers,every instance,operating systems and applications

    - Automate security best practices

    - Protect data in transit and at rest: Encryption,tokenization and access control

    - Keep people away from data: Reduce or eliminate the need for direct access or manual processing of data

    - Prepare for security events: Run incident response simulations and use tools with automation to increase your speed for detection,investigation and recovery

> > Security AWS Services

> Identity and access management:

    - IAM

    - AWS STS

    - MFA Token

    - AWS Organization

> Detective Controls:

    - AWS Config

    - AWS CloudTrail

    - Amazon CloudWatch

> Infrastructure Protection:

    - Amazon CloudFront

    - Amazon VPC

    - AWS Shield

    - AWS WAF

    - Amazon Inspector

> DATA Protection:

    - KMS

    - S3

    - Elastic Load balancing(ELB)

    - Amazon EBS

    - Amazon RDS

> Incident Response:

    - IAM

    - AWS CloudFormation

    - Amazon CloudWatch Events

### 3. Reliablity

> Ability of a system to recover from infrastructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues

> Design Principles:

    - Test Recovery Procedures: Use automation to simulate different failures or to recreate scenario that led to failures before

    - Automatically recover from failure: Anticipate and remediate failures before they occur

    - Scale Horizontally to increase aggregate system availablity: Distribute requests across multiple,smaller resources to ensure that they don't share common point of failure

    - Stop gussing capacity: Maintain the optimal level to satisfy demand without over or under provesioning

    - Use Auto Scaling

    - Manage change in automation: Use automation to make changes to infrastructure

> > Reliablity AWS Services

> Foundations:

    - IAM

    - Amazon VPC

    - Service limits

    - AWS Trusted Advisor

> Change Management:

    - AWS Auto Scaling

    - Amazon CloudWatch

    - AWS CloudTrail

    - AWS Config

> Failure Management:

    - Backups

    - AWS CloudFormation

    - Amazon S3

    - Amazon S3 Glacier

    - Amazon Route53

### 4. Performace Efficiency

> Includes the ability to use computing resources efficiently to meet system requirements and maintain that efficiency as demand changes and technologies evolve

> Design Principles:

    - Democratize advanced technologies: Advance technologies become services and hence you can focus more on product development

    - Go Global in minutes: Easy deployment in multiple regions

    - Use Serverless architectures: Avoid burden of managing servers

    - Experiment more often: Easy to carry out comparative testing

    - Mechanical Sympathy: Be aware of all AWS Services

> > Performance Efficiency AWs Services

> Selection:

    - AWS Auto Scaling

    - AWS Lambda

    - Amazon Elastic Block Store (EBS)

    - Amazon Simple Storage Service (S3)

    - Amazon RDS

> Review:

    - AWS CloudFormation

    - Aws News Blog

> Monitoring:

    - Amazon CloudWatch

    - AWS Lambda

> Tradeoffs:

    - Amazon RDS

    - Amazon Elasticache

    - AWS Snowball

    - Amazon CloudFront

### 5. Cost Optimization

> Includes the ability to run systems to deliver business value at the lowest price point

> Design Principle:

    - Adopt a consumtion mode: Pay only for what you use

    - Measure overall efficiency: Use CloudWatch

    - Stop spending money on data center operations: AWS does the infrastructure part and enables customer to focus on organization projects

    - Analyze and attribute expenditure: Accurate identification of system usage and costs,helps measure return investment(ROI) - Make sure to use tags

    - Use managed and application level services to reduce cost of ownership: As Managed services operates at Cloud scale,they can offer a lower cost per transaction or service

> > Cost Optimization AWS Services

> Expenditure Awareness:

    - AWS Budgets

    - AWS Cost and Usage Report

    - AWS Cost Explorer

    - Reserved instance Reporting

> Cost-Effective Resources:

    - Spot Instance

    - Reserved Instance

    - Amazon S3 Glacier

> Matching supply and demand:

    - AWS Auto Scaling

    - AWS LAmbda

> Optimizing Over Time:

    - AWS Trusted Advisor

    - AWS Cost and Usage report

    - AWS News Blog

### 6. Sustainability

> the sustainability pillar focuses on minimizing the environmental impacts

> Design Principle:

    - Understand your impact: establish performance indicators,evaulate improvements

    - Establish sustainabilty goals: Set long-term goals for each workload,model return on investment(ROI)

    - Maximize utilization: Right size each workload to maximize the energy efficiency of the underlying hardware and minimize idle resources

    - Anticipate and adopt new,more efficient hardware and software offerings: and design for flexibility to adopt new technologies over time.

    - use managed service: Shared services reduce the amount of infrastructure,Managed services helps automate sustainability best practice as moving infrequent accessed data to cold storage and adjustting compute capacity

    - Reduce the downstream impact of your cloud workloads: Reduce the amount of energy or resources required to use your services and reduce the need for your customer to upgrade their devices

> > Sustainablity AWS Services

> EC2 Auto Scaling, Serverless Offerings:

    - Lambda

    - Fargate

    - EC2 Auto Scaling

> Costing:

    - Cost Explorer

    - EC2 (Graviton2)

    - EC2 Spot instances

> Storage:

    - EFS-IA

    - Amazon S3 Glacier

    - EBS Cold HDD voolumes

> S3 LifeCycle Configurations, S3 Intelligient Tiering

> Amazon Data LifeCycle Manager

> Read local, Write Global:

    - RDS Read Replicas

    - Aurora Global DB

    - Dynamo DB Global Table

    - CloudFront

# AWS Well-Architected Tool

> Free tool to review your architectures against the 6 pillars Well-Architected Framework and adopt architectural best practices

> How does it work?:

    - Select your workload and answer questions

    - Review your answers against 6 pillars

    - Obtain advice

    - get videos and documentations

    - generate a report,see the results in a dashboard

> [<b><u>for more</u></b>](https://console.aws.amazon.com/wellarchitected)

# AWS Cloud Adoption Framework (AWS CAF)

> Helps you build and then execute a comprehensive plan for your digital transformation through innovative use of AWS

> Created by AWS Professionals by taking advantage of AWS Best Practices and lessons learned from 1000s of customers

> AWs CAF identifies specific organizational capabilities that underpin successful cloud trnasformations

> AWS CAF groups its capabilities in six perspective:

* Business

* People

* Governance

* Platform

* Security

* Operations

> Business Prespective:

* Helps ensure that your cloud investments accelerate your digital transformation ambitions and business outcomes

> Business Capabilities:

* Strategy Management

* Portfolio Management

* Innovation Management

* Product Management

* Strategic Partenership

* Data Monetization

* Business Insight

* Data Science

> People Prespective:

* Serves as <b> a bridge between technology and business</b>, accelerating the cloud journey to help organizations more rapidly evolve to a culture of continuous growth, learning and where change becomes business-as-normal, with focus on culture, organizational structure, leadership and workforce

> People Capabilities:

* Culture Evolution

* Trnasformational Leadership

* Cloud Fluency

* Workforce Transformation

* Change Acceleration

* Organizational Design

* Organizational Alignment

> Governance Prespective:

* helps you orchestrate your cloud initiatives while maximizing organizational benefits and minimizing transformation releted risks.

> Governance Capabilities:

* Program and Project Management

* Benefits Management

* Risk Management

* Cloud Financial Management

* Application Portfolio Management

* Data Governance

* Data Curation

> Platform Prespective

* helps you build an enterprise-grade, scalable, hybrid cloud platform, modernize existing workloads and implement new cloud-native solutions

> Platform Capabilities:

* Platform Architecture

* Data Architecture

* Platform Engineering

* Data Engineering

* Provisioning and Orchestration

* Modern Application Development

* Continuous Integration and Continuous Delivery

> Security Prespective

* helps you achive the confidentiality, integrity and availablity of your data and cloud workloads

> Security Capabilities:

* Security Governance

* Security Assurance

* Identity and Access Management

* Threat Detection

* Vulnerability Management

* Infrastructure Protection

* Data Protection

* Application Security

* Incident Response

> Operations Prespective

* helps ensure that your cloud services are delivered at a level that meets the needs of your business.

> Operations Capabilities:

* Observability

* Event Management (AIOps)

* Incident and Problem Management

* Change and Release Management

* Performance and Capacity Management

* Configuration Management

* Patch Management

* Availability and Continuity Management

* Application Management

### AWS CAF - Transformation Domains

> `Technology:`

* Using the cloud to migrate and modernize legacy infrastructure, applications, data and analytics platforms..

> `Process:`

* Digitizing, automating and optimizing your business operations
* leveraging new data and analytics platform to create actionalble insights
* using machine learning (ML) to improve your customer service experience..

> `Organization:`

* Reimagining your operating model
* Organizing your teams around products and value streams
* Leveraging agile methods to rapidly iterate and evolve

> `Product:`

* reimagining your business model by creating new value propositions (Product and services) and revenue models.

### AWS CAF - Transformation Phases

> > Envision:

* Demonstarte how the Cloud will accelerate business outcomes by identifying transformation opportunities and create a foundation for your digital transformation

> > Align:

* Identify capability gaps across the 6 AWS CAF Prespectives which results in an action Plan

> > Launch:

* Build and deliver pilot initiatives in production and demonstrate incremental business value

> > Scale:

* Expand pilot initiatives to the desired scale while realizing the desired business benefits

# AWS Right Sizing

> EC2 has many instance types, but choosing the most powerful instance type isn't the best choice, because the cloud is elastic

> Right Sizing is the process of matching instance types and sizes to your workload performance and capacity requirements at the <b>lowest possible cost</b>

> Scaling up is easy so always start small

> It's also the process of looking at deployed instances and identifying opportunities to eliminate or downsize without compromising capacity or other requirements, which results in lower costs

> it's important to Right Size...

* before a Cloud Migration
* Continuously after the cloud onboarding process

* - CloudWatch, Cost Explorer, Trusted Advisor, 3rd party tools can help

### AWS EcoSystem - Free Resources

* [<u><b>AWS Blogs</b></u>](https://aws.amazon.com/blogs/aws)
* [<u><b>AWS Forums(Community)</b></u>](https://forums.aws.amazon.com/index.jspa)
* [<u><b>AWS Whitepapers and Guide</b></u>](https://aws.amazon.com/whitepapers)
* [<u><b>AWS Partener Solutions (formerly Quick Start)</b></u>](https://aws.amazon.com/quickstart/)
* - Automated gold-standard deployments in the AWS Cloud
* - Build you productions environments quickly with templates
* - Leverages CloudFormation
* [<u><b>AWS Solutions</b></u>](https://aws.amazon.com/solutions/)
* - Vetted Technology Solutions for the AWS Cloud
* Example: [<u><b>AWS Landing Zone</b></u>](https://aws.amazon.com/solutions/implementaions/aws-landing-zone/)
* - secure, Multi account AWS Environment
* - <b>Replaced</b> by <b>AWS Control Tower</b>

### AWS EcoSystem - AWS Support

| tier       | Description                                                     |
| ---------- | --------------------------------------------------------------- |
| Developer  | Business hours email access to Cloud Support Associates         |
|            | General Guidance: < 24 business hours                           |
|            | System impaired: < 12 business hours                            |
|            |                                                                 |
| Business   | 24x7 Phone Email access to Cloud Support Engineers              |
|            | Production System Impaired: < 4 hours                           |
|            | Production System Down: < 1 Hour                                |
|            |                                                                 |
| Enterprise | Access to Techinal Account Manager (TAM)                        |
|            | Concierge Support Team (for billing and account best practices) |
|            | Business Critical System Down: < 15 Minutes                     |

<!-- https://www.tablesgenerator.com/markdown_tables -->

# AWS Marketplace

> Digital Catalog with thousands of software listings from <b> independent Software venodrs </b>(3rd Party)

> Example:

* Custom AMI (Custom OS, firewalls, technical solutions..)
* CloudFormation templates
* Software as a Service
* Containers
* if you buys through the AWS Marketplace, it goes into your AWS bill
* You can sell your own solutions on the AWS Marketplace

### AWS Training

> AWS Digital(online) & classroom Training (in-person/virtual)

> AWS Private Training(for your organization)

> Training and Certification for U. S Government

> Training and Certification for the Enterprise

> AWS Academy: helps universities teach AWS

## AWS Professional Services and Partner Network

* The AWS Professional Services organization is a global team of experts
* They work alongside your team and a chooses member of the APN
* APN = AWS Partner Network
* <b>APN Technology Partners: </b>Providing hardware, connectivity and software
* <b>APN Consulting Partners: </b>Professional services firm to help build on AWS
* <b>APN Training Partners: </b>find who can help you learn AWS
* <b>AWS Competency Program </b>AWS Competencies are granted to APN Partners who have demonstrated techincal proficiency and proven customer success in specialized solution areas.
* <b>AWS Navigate Program:</b> help partners become better partners

## AWS Knowledge Center

> Contains the most frequent and common questions and requests:

* [<b><u>Visit here</u></b>](https://aws.amazon.com/premiumsupport/knowledge-center/)

## AWS IQ

* Quickly find professional help for your AWS projects
* Engage and pay AWS Certified 3rd party experts for on-demand project work
* Video-conferencing, contract management, secure collaboration, integrated billing
* for Customers:
* - Submit Request -> Review Responses -> Select Expert -> Work Securely -> Pay per Milestone
* For Experts:
* - Create Profile -> Connect with Customers -> Start a proposal -> Work Securely -> get paid

## AWS re:Post

> <b>AWS-managed Q&A service</b> offering crowd-sourced, expert-reviewed answers to your techinical questions about AWS that replaces the original AWS Forums

* Part of AWS Free Tier
* Community members can earn reputation points to build up their community expert status by providing accepted answers and revirwing answers from other users

> <b>Questions from AWS Premium Support customers that do not receive a response from the community are passed on to AWS Support engineers</b>

* AWS re:post is not intended to be used for questions that are time-sensitive or involve any proprietary information

## AWS Managed Services (AMS)

> Provides infrastructure and application support on AWS

> AMS offers a team of AWS experts who manage and Operate your infrastructure for security, reliablity and availablity

> Helps organizations offload routine management tasks and focus on their business objective

> Fully Managed services, so AWS handle common activities such as change requests, monitoring, path management, security and backup services

> Implements best practices and maintains your AWS infrastructure to reduce your operational overhead and risk

> AMS Business hours are 24/365

