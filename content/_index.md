+++
title = "Serverless Web Application Building on AWS"
date = 2024
weight = 1
chapter = false
+++

# Serverless Web Application Building on AWS

### Workshop Overview

#### Serverless Architecture of the Workshop

![Serverless-FCJ](/images/1/Serverles.png?width=90pc)

#### Objectives of the Workshop

The main goal of the workshop "Serverless Web Application Building on AWS" is to help participants understand how to build a serverless architecture on AWS with integrated services, ensuring cost optimization, security, and scalability.

#### Knowledge provided in the Workshop

**AWS Services and Costs:**

1.  **Amazon Route 53**: is a highly scalable DNS (Domain Name System) service of AWS. It helps convert easy-to-remember domain names that users type into their browsers into the IP addresses of AWS resources.

    - Functionality: Route 53 ensures the routing of traffic to the right AWS resources with high reliability and speed. It also offers DNS management, health checks, and geo-based routing, which optimizes the global user experience.
    - Free Tier: 1 million free standard DNS queries monthly.

      **_Standard price:_**

      - $0.50/month per managed domain.
      - $0.40 for each subsequent million queries (in addition to the free 1 million).

2.  **AWS CloudFront**: An AWS content delivery network (CDN) that delivers static content such as images, videos, and documents from servers closest to users.

    - Functions: Reduce latency, increase application access speed for users around the world. It also integrates with AWS security services such as AWS WAF and AWS Shield to protect content from online threats.
    - Free Tier: 1 TB of data transfer and 2 million free HTTP/HTTPS requests for the first 12 months.

      **_Standard price:_**

      - $0.085/GB for the first 10 TB.
      - $0.0075/10,000 HTTP/HTTPS requests.

3.  **Amazon S3**: AWS highly scalable object storage service designed to store and retrieve any amount of data from anywhere on the web.

    - Function: Data storage and retrieval. S3 provides reliable, highly secure storage at a reasonable cost. You only pay for the amount and amount of data used, which optimizes operating costs.
    - Cost Optimization: Multi-layer storage (S3 Standard, S3 Glacier) for lower costs.
    - Free Tier: 5 GB of standard storage (S3 Standard) for free for the first 12 months.

      **_Standard price:_**

      - $0.023/GB for S3 Standard (less than the first 50 TB per month).
      - S3 Glacier for long-term storage has a lower cost, around $0.004/GB per month.

4.  **AWS WAF (Web Application Firewall)**: A web application firewall that helps protect web applications from common attacks such as SQL injection and cross-site scripting (XSS).

    - Function: Block malicious requests before they reach the app. WAFs allow you to create custom security rules to protect your applications, while also providing traffic monitoring and preventing threats before they can cause damage.

      **_Standard price:_**

      - $5.00/month per Web ACL (Access Control List).
      - $0.60 per million requests evaluated by ACLs.

5.  **AWS Certificate Manager**: Makes it easier to manage SSL/TLS certificates, from issuance, renewal, to deploying them on other AWS services such as CloudFront.

    - Function: Secure connections between users and CloudFront. Automated SSL/TLS certificate management secures communication between your users and applications without having to worry about manually renewing or configuring certificates.
    - Free Tier: Provides and manages SSL/TLS certificates for free when used with AWS services such as CloudFront and Elastic Load Balancing.

      **_Standard price:_** There is no cost for SSL/TLS certificates used in AWS services.

6.  **Amazon Cognito**: Provides user management and authentication services that allow users to securely register, log in, and access resources.

    - Functionality: Cognito simplifies user management, and integrates with other AWS services to provide comprehensive security and easy access management.
    - Free Tier: 50,000 user authentication requests per month.

      **_Standard price:_**

      - $0.0055 for each authentication request that exceeds 50,000.

7.  **AWS API Gateway**: A bridge between users and a serverless backend (Lambda) and a powerful AWS API management service that helps you create, deploy, and manage RESTful APIs with ease.

    - Function: Handles API requests from users, authentication, and delivery to Lambda. API Gateway provides traffic management, performance monitoring, and API security, helping to ensure that your application can handle millions of requests with high reliability and performance.
    - Cost optimization: Pay only when there is an API request.
    - Free Tier: 1 million free REST or HTTP API calls per month.

      **_Standard price:_**

      - $3.50 per million subsequent API calls.

8.  **AWS Lambda**: The primary serverless platform for running code without server management. All you need to do is provide the code, and Lambda will automatically handle everything needed to run and scale the code.

    - Function: Handles requests sent from API Gateway. With Lambda, you pay only for the execution time of your code, which optimizes costs and eliminates the need to manage infrastructure. Lambda also automatically scales to meet the needs of the application.
    - Cost Optimization: Pay based on runtime and number of requests.
    - Free Tier: 1 million requests and 400,000 GB-s of compute time per month.

      **_Standard price:_**

      - $0.20 for every 1 million requests.
      - $0.00001667 per GB-s of compute time.

9.  **DynamoDB**: is a highly scalable NoSQL database designed to handle any workload with low latency.

    - Functionality: DynamoDB provides reliable performance, with auto-scaling, helping you build applications that can handle millions of requests per second without performance struggles.
    - Free Tier: 25 GB of storage and 2.5 million read/write requests per month in the AWS free plan (12 months).

      **_Standard price:_**

      - Write Request Units (WRU): $1.25 per million write requests.
      - Read Request Units (RRU): $0.25 per million read requests.
      - Storage: $0.25/GB per month.

10. **Amazon SNS (Simple Notification Service)**: A reliable, cross-platform notification service that integrates with serverless applications. SNS allows you to send notifications from the system to users via email, SMS, or to other systems.

    - Function: Send notifications via SMS, HTTP/HTTPS, or other protocols to users or automated systems. SNS helps ensure that important notifications and information are sent quickly and efficiently, supporting the tracking and management of application activity.
    - Free Tier: 1 million free requests per month and 1,000 free SMS notifications sent from SNS per month (depending on the region).

      **_Standard price:_**

      - Requests: $0.50 for every 1 million requests.
      - Send SMS: SMS prices vary by region and carrier (e.g., $0.02018 per SMS in Singapore).
      - HTTP/HTTPS, SQS, Lambda, Mobile Push: There is no charge for sending notifications to these services.

#### Workshop Services and Costs Reference

**Service Documentation:**

- [Uploading objects - Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html)
- [Tutorials - Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Tutorials.html)
- [Improve Your Architecture With Amazon CloudFront](https://catalog.us-east-1.prod.workshops.aws/workshops/4557215e-2a5c-4522-a69b-8d058aba088c/en-US/basic-configuration)
- [API Gateway REST APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-rest-api.html)
- [Building Lambda functions with Python](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html)
- [Use AWS WAF protections](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-awswaf.html)
- [DNS validation - AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/dns-validation.html)
- [Amazon Cognito - Control access to REST APIs using Amazon Cognito user pools as an authorizer](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.html)
- [How to use Amazon SNS with AWS Lambda Function](https://medium.com/cloudnloud/how-to-use-aws-lambda-function-with-amazon-sns-e8fe38097725)
- [Working with tables and data in DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html)

**Cost Documentation:**

- [Amazon S3 pricing](https://aws.amazon.com/s3/pricing/?nc1=h_ls)
- [Amazon Route 53 pricing](https://aws.amazon.com/route53/pricing/?nc1=h_ls)
- [Amazon CloudFront Pricing](https://aws.amazon.com/cloudfront/pricing/?nc1=h_ls)
- [Amazon API Gateway pricing](https://aws.amazon.com/api-gateway/pricing/?nc1=h_ls)
- [AWS Lambda Pricing](https://aws.amazon.com/lambda/pricing/?gclid=Cj0KCQjw9Km3BhDjARIsAGUb4nzp-WTaIsbYgmhOZEnZJr5CLj-M8FKIYFIDZDBw4NB4HwbzwsEAEiMaAprbEALw_wcB&trk=cc9d3bb4-0a21-43d0-8236-0f2deaffe082&sc_channel=ps&s_kwcid=AL!4422!3!651510255297!p!!g!!lambda&ef_id=Cj0KCQjw9Km3BhDjARIsAGUb4nzp-WTaIsbYgmhOZEnZJr5CLj-M8FKIYFIDZDBw4NB4HwbzwsEAEiMaAprbEALw_wcB:G:s&s_kwcid=AL!4422!3!651510255297!p!!g!!lambda!19828212645!149982299911)
- [AWS WAF Pricing](https://aws.amazon.com/waf/pricing/?nc1=h_ls)
- [AWS Certificate Manager pricing](https://aws.amazon.com/certificate-manager/pricing/?nc1=h_ls)
- [Amazon Cognito pricing](https://aws.amazon.com/cognito/pricing/?nc1=h_ls)
- [Amazon SNS pricing](https://aws.amazon.com/sns/pricing/?nc1=h_ls)
- [Amazon DynamoDB pricing](https://aws.amazon.com/dynamodb/pricing/?nc1=h_ls)

### Content

1. [Introduction](1-introduction)
2. [Preparation Steps](2-preparation)
3. [Front-end deployment](3-deployment-frontend)
4. [Initialize SNS](4-sns)
5. [Initialize Cognito](5-cognito)
6. [Initialize DynamoDB](6-dynamodb)
7. [Deploy Lambda function](7-lambda-function)
8. [Setting up API Gateway](8-api-gateway)
9. [Check Web Application](9-test-webapp)
10. [Clean up resources](10-clean-resource)
