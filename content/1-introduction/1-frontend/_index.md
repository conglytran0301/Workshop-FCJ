+++
title = "Routing, Content Distribution, and Security"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1.1 </b>"
+++

### Overview

**1. Route53:** is a highly scalable DNS (Domain Name System) service from AWS. It helps convert easy-to-remember domain names that users type into their browsers into the IP addresses of AWS resources.

Benefits: Route 53 ensures the routing of traffic to the right AWS resources with high reliability and speed. It also offers DNS management, health checks, and geo-based routing, which optimizes the global user experience.

**2. CloudFront:** is an AWS content delivery network (CDN) that delivers static content such as images, videos, and documents from the servers closest to the user.

Benefits: CloudFront minimizes latency and speeds up website loading thanks to global edge locations. It also integrates with AWS security services such as AWS WAF and AWS Shield to protect content from online threats.

**3. S3 (Simple Storage Service):** is AWS's highly scalable object storage service, designed to store and retrieve any amount of data from anywhere on the web.

Benefits: S3 provides reliable, highly secure storage at a reasonable cost. You only pay for the amount and amount of data used, which optimizes operating costs.

**4. WAF (Web Application Firewall):** is a web application firewall that helps protect web applications from common attacks such as SQL injection and cross-site scripting (XSS).

Benefits: WAFs allow you to create custom security rules to protect your applications, while also providing the ability to monitor traffic and prevent threats before they can cause damage.

**5. AWS Certificate Manager:** makes it easier to manage SSL/TLS certificates, from issuance, renewal, to deploying them on other AWS services such as CloudFront.

Benefits: Automated SSL/TLS certificate management secures communication between your users and applications without having to worry about manually renewing or configuring certificates.

### Reference Links

- [Tutorials - Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Tutorials.html)
- [Improve Your Architecture With Amazon CloudFront](https://catalog.us-east-1.prod.workshops.aws/workshops/4557215e-2a5c-4522-a69b-8d058aba088c/en-US/basic-configuration)
- [Uploading objects - Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html)
- [Use AWS WAF protections](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-awswaf.html)
- [DNS validation - AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/dns-validation.html)
