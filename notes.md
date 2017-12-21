## 10,000 ft Overview

### Compute
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

### Storage
* S3 - Simple Storage Service
    * Buckets that you can upload files to
* EFS - Elastic File System
    * Let's you use multiple machines
* Glacier - Data Archival
* Snowball - Bring in large amounts of data to AWS data-center
* Storage Gateway - Virtual Appliances
    * Replicate information back to S3

### Databases
* RDS - Relation Database Service
    * MySQL, PostgreSQL, etc
* Elsaticache - Caching service commonly queried things from you database
* DynamoDB - Non relational databases
* Red Shift - Data Warehousing

### Migration
* AWS Migration Hub - Tracking Service
    * Track applications as you migrate them AWS
    * Allows you to visualize your migration
* Application Discover Service - Detects applications and their dependencies
* Database Migration Service - Migrate your DB from on premise into AWS
* Server Migration Service - Similar to db migration service
* Snowball - In between storage and migration for large amounts of data to the cloud

### Networking & Content Delivery
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

### Management Tools 
* CloudWatch
* CloudFormation
* CloudTrail
* Config
* OpsWorks
* Service Catalog
* Systems Manager
* Trusted Advisor
* Managed Services 

### Media Services
* Elastic Transcoder
* MediaConvert
* MediaLive
* MediaPackage
* MediaStore
* MediaTailor

### Machine Learning
* SageMaker
* Comprehend
* DeepLens
* Lex
* Machine Learning
* Polly
* Rekognition
* Amazon Translate

### Analytics
* Athena 
* EMR
* CloudSearch
* ElasticSearch Service
* Kinesis
* Kinesis Video Streams
* QuickSight
* Data Pipeline
* Glue