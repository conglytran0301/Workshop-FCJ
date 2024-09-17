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

#### Reference Links

- [Uploading objects - Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html)
- [Improve Your Architecture With Amazon CloudFront](https://catalog.us-east-1.prod.workshops.aws/workshops/4557215e-2a5c-4522-a69b-8d058aba088c/en-US/basic-configuration)
- [Tutorials - Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Tutorials.html)
- [DNS validation - AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/dns-validation.html)
- [Use AWS WAF protections](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-awswaf.html)
