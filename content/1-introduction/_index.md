+++
title = "Introduction"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

### Workflow

**1. User Accesses the Application via Web Browser**

- When a user wants to access the application, they enter the website URL in the browser. This can be a website providing static content (HTML, CSS, JavaScript) or interactive features like login, registration, or data manipulation. The access request is sent from the browser over the Internet to the AWS system for processing.

**2. Route 53 Resolves Domain Name and Directs Request**

- First, the request from the browser is sent to Amazon Route 53, AWS’s DNS (Domain Name System) service. Route 53's job is to resolve the domain name of the application into a specific IP address, helping to route traffic to the correct resources in the AWS system. Route 53 can be configured to support load balancing between multiple servers or geographical regions to optimize access speed and ensure high availability.

- Once the domain is resolved, the user's request is forwarded to CloudFront, AWS’s content delivery network (CDN).

**3. CloudFront Receives Request and Checks Cache**

- Amazon CloudFront acts as a Content Delivery Network (CDN), distributing content from edge locations (network points closest to the user) to reduce latency and improve website performance.

- When CloudFront receives the request from the user, it checks if static resources (like HTML, CSS, JavaScript files, images) are available in the cache of the closest edge location. If the resource is cached, CloudFront returns it immediately without needing to access the backend, reducing response time.

- If the resource is not cached, CloudFront fetches the static files from Amazon S3, the main storage for the application’s static content, and delivers it to the user.

**4. Amazon S3 Supplies Static Content to CloudFront**

- Amazon S3 (Simple Storage Service) is used to store static files for the application such as images, videos, CSS, and JavaScript. It’s a highly durable and scalable storage service. When CloudFront doesn’t find the resource in its cache, it requests the static content from S3 and caches it temporarily for future requests.

**5. Web Application Firewall (WAF) Protects the System**

- AWS WAF (Web Application Firewall) is integrated with CloudFront to protect the system from common attacks, such as SQL Injection, Cross-Site Scripting (XSS), and DDoS (Distributed Denial of Service) attacks.

- WAF can be configured with specific security rules to inspect and block malicious requests before they reach the application, thus safeguarding the system from common vulnerabilities.

**6. Certificate Manager Handles SSL Certificates for Data Encryption**

- Amazon Certificate Manager (ACM) manages SSL/TLS certificates for the system, ensuring that all communications between the user and the system are encrypted, protecting information from man-in-the-middle attacks.

- Certificate Manager automatically handles SSL certificate management and renewal to ensure secure connections are always functional. This is especially crucial in environments where high data security is required.

**7. User Authentication via Cognito User Pool**

- For requests requiring authentication (e.g., login, registration), the user interacts with Amazon Cognito User Pool, a user identity management service.

- Cognito allows users to log in or sign up for accounts on the application. When the user provides login credentials (email, password), Cognito authenticates the credentials and issues JWT tokens to authorize subsequent requests from the user.

- Additionally, Cognito supports multi-factor authentication (MFA) and integrates with external services like Facebook, Google for convenient user login.

**8. API Gateway Handles Dynamic Requests from Users**

- For complex requests such as retrieving data from a database or processing backend tasks, the user’s request is sent from the browser via API Gateway.

- Amazon API Gateway acts as a gateway between the user and backend services. It receives HTTP(S) requests and forwards them to AWS Lambda for processing. API Gateway can integrate with Cognito to verify user tokens before granting access to sensitive resources.

- Additionally, API Gateway supports version control for APIs, throttling, and request monitoring to ensure performance and security.

**9. Lambda Executes Business Logic**

- AWS Lambda is a serverless compute service that only runs when triggered by events. When API Gateway forwards a request from the user, Lambda executes the business logic of the application without the need to manage servers.

- Lambda can perform various tasks such as handling login information, retrieving data from the database, or invoking other services for complex processing. Lambda automatically scales to meet the demand and charges only for the execution time, making it cost-effective for the system.

**10. DynamoDB Stores and Retrieves Dynamic Data**

- Amazon DynamoDB is a NoSQL database that offers flexible scaling. When Lambda needs to retrieve or write data, it interacts with DynamoDB.

- DynamoDB stores the dynamic data of the application, such as user information, transaction states, or application-related data. DynamoDB supports very fast read/write speeds and handles large data volumes, ensuring smooth operation even when many users access the application simultaneously.

**11. SNS Sends Notifications**

- When important events or state changes occur in the application (e.g., a new user registration or a new order), Lambda can trigger Amazon SNS (Simple Notification Service) to send notifications.

- SNS can send notifications through various channels such as email, SMS, or to other systems using a pub/sub mechanism. This allows the application to provide real-time information to users or administrators.

**12. User Receives Response**

- After the requests have been processed by Lambda and data has been retrieved from DynamoDB or other sources, API Gateway receives the response from Lambda and forwards the results back to the user’s browser.

- Finally, the user receives the data they requested, or relevant notifications (such as account registration confirmation, order updates, etc.).

![Serverless-FCJ](/images/1/Serverles.png?width=90pc)

### Summary

Each step in the system plays a crucial role in handling user requests from accessing the website, sending requests, to receiving responses. The serverless system leverages services like CloudFront, Lambda, and API Gateway to reduce infrastructure management while ensuring the application’s performance and security. Components such as Cognito, DynamoDB, and SNS provide easy user management, data storage, and notification capabilities, allowing for the development of a highly scalable and robust distributed application.

### Content

1. [Routing, Content Distribution, and Security](1-introduction/1-frontend)
2. [Logic Processing, User Management, and System Interaction](1-introduction/2-system)
