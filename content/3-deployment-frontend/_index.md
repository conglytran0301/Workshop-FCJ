+++
title = "Front-end Web Deployment"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

The web frontend in this architecture is the user interface part of the application, which is deployed and managed on AWS services to ensure efficiency and security. Frontend static content, including HTML, CSS, and JavaScript, is stored on an object hosting service, which is then delivered to users through a content delivery network (CDN). This helps to ensure that the website loads quickly and works stably across the globe. For security, the frontend is protected by a web application firewall (WAF) and uses SSL/TLS certificates, which are managed through AWS services, ensuring user data is encrypted and secure. In addition, the AWS DNS system is configured to direct domain names to the necessary resources, creating a robust and secure frontend web architecture.

### Content

1. [Initialize an S3 Bucket](3-deployment-frontend/1-S3-Bucket)
2. [Configure Cloudfront](3-deployment-frontend/2-Cloudfront)
3. [Configure Route 53 and Certificate Manager](3-deployment-frontend/3-Route53-ACM)
4. [WAF Initialization](3-deployment-frontend/4-WAF)
