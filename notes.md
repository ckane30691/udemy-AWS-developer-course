## 10,000 ft Overview

### **Compute**
* EC2 - Elastic Compute Cloud
    * Virtual machines inside AWS platform
* EC2 Container Service - Run & Manage Docker Containers at scale
* Elastic Beanstalk - For Developers who don't want to learn AWS
* Lambda - Code you upload to the cloud that you control when it executes
    * You can use lambda to creat serverless websites
* Lightsail - For people who really don't want to understand AWS
    * Virtual Private Service
    * Watered down version of EC2
* Batch - Used for batch computing in the cloud

### **Storage**
* S3 - Simple Storage Service
    * Buckets that you can upload files to
* EFS - Elastic File System
    * Let's you use multiple machines
* Glacier - Data Archival
* Snowball - Bring in large amounts of data to AWS data-center
* Storage Gateway - Virtual Appliances
    * Replicate information back to S3

### **Databases**
* RDS - Relation Database Service
    * MySQL, PostgreSQL, etc
* Elsaticache - Caching service commonly queried things from you database
* **DynamoDB** - Non relational databases
* Red Shift - Data Warehousing

### Migration
* AWS Migration Hub - Tracking Service
    * Track applications as you migrate them AWS
    * Allows you to visualize your migration
* Application Discover Service - Detects applications and their dependencies
* Database Migration Service - Migrate your DB from on premise into AWS
* Server Migration Service - Similar to db migration service
* Snowball - In between storage and migration for large amounts of data to the cloud

### **Networking & Content Delivery**
* VPC - Virtual Data Center
    * This where you configure a lot of things
    * Very important to understand for the exam
* CloudFront - Amazon's content Delivery Network
    * Allows media content to be served at Edge locations close to the user
* Route53 - AWS DNS service
* API Gateway - Way of creating your own APIs for other services to talk to
* Direct Connect - Way of running a dedicated line from your HQ directly to Amazon

### Developer Tools - Not featured in the exam
* CodeStar - Project management for your code
    * Collab tool
* CodeCommit - Place to store your code
    * Similar to git/github
* CodeBuild - Compiles your code and runs tests for you
* CodeDeploy - Automates application deployments to your EC2 instances
* CodePipeline - Continuous delivery service
* X-Ray - Debug and analyze tool
* Cloud9 - IDE environment for AWS

### **Management Tools**
* CloudWatch - Monitoring Service
    * SysOps exam
* CloudFormation - Solutions Architect
    * Way of scripting infrastructure
    * Lets you deploy sites with templates
* CloudTrail - Logs changes to your AWS environment for 1 week by default
* Config - Monitors config of entire AWS environment
    * Has snapshots of your AWS environment
* OpsWorks - Like elastic beanstalk
    * Way of automating the config of your environments
* Service Catalog - Catalog of IT Services that are approved for use
    * VMS, Multi-tier architecture
* Systems Manager - Interface for managing AWS resources
    * Lets you group resources
* Trusted Advisor - Gives you advice across multiple different disciplines in your AWS enviro.
* Managed Services - Manages your AWS stuff for you

### Media Services
* Elastic Transcoder - Resizes videos for all the different types of devices
* MediaConvert - Let's you create video content at scale
* MediaLive - High quality video streams
* MediaPackage - Prepares and protect vids for delivery over the internet
* MediaStore - Storage optimized for video
* MediaTailor - Lets you do targeted adverts into vid streams

### Machine Learning
* SageMaker - Lets devs use deep learning
* Comprehend - Does data sentiment analysis
* DeepLens - Artificially aware camera
    * Physical piece of hardware that you can buy
* Lex - Powers the amazon alexa service
    * AI way of interfacing with customers
* Machine Learning - Basic machine learning without using hidden layers
* Polly - Takes text and turns it into speech
* Rekognition - Used for image and video recognition
* Amazon Translate - Just like google translate
* Amazon Transcribe - Auto speech recognition from vid files and mp3s

### **Analytics**
* Athena - Lets you run SQL Queries against things in your S3 bucket
    * Serverless
* EMR - Elastic MapReduce
    * Used for big data
* CloudSearch - AWS Search Service
* ElasticSearch Service - AWS Search Service
* Kinesis - Way of ingesting large amounts of data (i.e. social media feeds or tweets) into AWS
* Kinesis Video Streams - Lets you take in live streams and do processing on it
* QuickSight - Biz Intelligence Tool
* Data Pipeline - Lets you move data between different AWS Services
* Glue - Used to extract, transform, and load data into the format you want

### **Security & Identity & Compliance**
* IAM - Identity access management
* Cognito - Device Authentication for mobile apps
* GuardDuty - Monitors for malicious activity on your AWS acct
* Inspector - Agent you install on your VM that you can run tests against
    * You can schedule this to run and it will generate reports
* Macie - Scans your S3 buckets and looks for things that are personably identifiable and will alert you
* Certificate Manager - Get free SSLs if you use Route53
* CloudHSM - Hardware Security Module
    * Store keys for encryption
* Directory Service - Integrates Microsoft Acitve Directory with AWS
* WAF - Web Application Firewall to stop things like SQL injections and cross-site scripting attacks
* Shield - DDOS Mitigation
    * Advanced Shield: Dedicated watcher to prevent DDOS attacks
* Artifact - Portal for on demand access to AWS compliance reports

### Mobile Service
* Mobile Hub - Management Console for mobile apps
* Pinpoint - Lets you use mobile push notifications to drive user traffic
* AWS AppSync - Auto updates data in web and mobile apps in real time
* Device Farm - Lets you test your app on actual mobile devices
* Mobile Analytics - Self explanatory

### AR & VR
* Sumerian - Lets you use a common set of tools for AR, VR, & 3D apps

### **Application Integration**
* Step Functions - Lets you manage your different lambda functions
* Amazon MQ - Message Queues
* SNS - Notifications Service
* SQS - Lets you decouple your infrastructure
* SWF - Simple Work Flow Service
    * This is the process for when you order a package

### Customer Engagement
* Connect - Contact Center as a Service
    * Like having your own call center at any scale
* Simple Email Service - Lets you send large amounts of email at scale

### Biz Productivity
* Alexa for Biz - Lets you connect Alexa to your internal biz
* Chime - Like google hangouts
* Work Docs - Like dropbox but for AWS
* WorkMail - like Microsoft Office 365

### Desktop & App Streaming
* Workspaces - VDI solution
    * Lets you run an entire OS in the cloud
* AppStream 2.0 - Streams an app to your device via the cloud

### Internet of Things
* IOT - Lets you connect millions of devices sending back data like video, temp, audio, etc
* IOT Device Management - Lets you manage all your connected devices
* Amazon FreeRTOS - OS for your micro controllers
* Greengrass - Software that lets you run local compute message data caching sync for connected devices in a secure way

### Game Dev
* GameLift - Service for developing games

## Identitiy Access Management 101
- Allows you to manage users and their level of access to the AWS console

### What does IAM give you?
* Centralized control of your AWS Account
* Shared access to your AWS Account
* Granular Permissions
* Identity Federation (including ActiveDirectory, Facebook, LinkedIn, etc)
* Multifactor Authentication
* Provides temporary access for users/devices and services where necessary
* Allows you to set up your own password rotation policy
* Integrates with many other AWS services
* Support PCI DSS Compliance

### Critical Terms
* Users - end users
* Groups - A collection of users under one set of permissions
* Roles - You create roles and can then assign them to AWS
* Policies - Document that defines one or more permissions