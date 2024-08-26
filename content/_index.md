+++
title = "AWS Serverless web app basic"
date = 2024
weight = 1
chapter = false
+++

# Serverless Web Application Building on AWS

#### Overview

In this article, we will build a Web application system that uses serverless services on the AWS platform. It leverages services such as S3 for static content storage, API Gateway for managing and routing API requests, Lambda for business logic processing, and DynamoDB for dynamic data storage. Additional services such as Route53, CloudFront, and WAF help ensure high performance and security for applications. In addition, Cognito is used to manage user authentication, and SNS helps send instant notifications. Overall, this architecture provides flexibility, scalability, and cost-effectiveness, while optimizing user experience and system security.

![Serverless-FCJ](/images/1/Serverles.png?width=90pc)

#### Content

1. [Introduction](1-introduction/)
2. [Preparation Steps](2-preparation>)
3. [Front-end deployment](3-deployment-frontend/)
4. [SNS Initiation](4-sns/)
5. [Cognito Initialization](5-cognito/)
6. [Initializing DynamoDB](6-dynamodb/)
7. [Implementing a Lambda function](7-lambda-function/)
8. [Setting up API Gateway](8-api-gateway/)
9. [Check Web Application](9-test-webapp/)
10. [Clean up resources](10-clean-resource/)
