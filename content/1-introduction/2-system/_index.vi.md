+++
title = "Xử lý Logic, Quản lý Người dùng và Tương tác Hệ thống"
date = 2020-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

### Tổng quan

**1. API Gateway:** là dịch vụ quản lý API mạnh mẽ của AWS, giúp bạn tạo, triển khai và quản lý các API RESTful một cách dễ dàng.

Lợi ích: API Gateway cung cấp khả năng quản lý lưu lượng, giám sát hiệu suất, và bảo mật API, giúp đảm bảo rằng ứng dụng của bạn có thể xử lý hàng triệu yêu cầu với độ tin cậy và hiệu suất cao.

**2. Lambda:** là dịch vụ điện toán không máy chủ (serverless), cho phép bạn chạy mã mà không cần quản lý máy chủ. Bạn chỉ cần cung cấp mã và Lambda sẽ tự động xử lý mọi thứ cần thiết để chạy và mở rộng mã.

Lợi ích: Với Lambda, bạn chỉ trả tiền cho thời gian thực thi của mã, giúp tối ưu hóa chi phí và loại bỏ nhu cầu quản lý cơ sở hạ tầng. Lambda cũng tự động mở rộng quy mô để đáp ứng nhu cầu của ứng dụng.

**3. DynamoDB:** là cơ sở dữ liệu NoSQL có khả năng mở rộng cao, được thiết kế để xử lý mọi khối lượng công việc với độ trễ thấp.

Lợi ích: DynamoDB cung cấp hiệu suất đáng tin cậy, với khả năng tự động mở rộng quy mô, giúp bạn xây dựng các ứng dụng có thể xử lý hàng triệu yêu cầu mỗi giây mà không gặp khó khăn về hiệu suất.

**4. Cognito:** cung cấp các dịch vụ quản lý người dùng và xác thực, cho phép người dùng đăng ký, đăng nhập, và truy cập các tài nguyên một cách an toàn.

Lợi ích: Cognito giúp đơn giản hóa việc quản lý người dùng, đồng thời tích hợp với các dịch vụ AWS khác để cung cấp bảo mật toàn diện và quản lý quyền truy cập dễ dàng.

**5. SNS (Simple Notification Service):** là dịch vụ nhắn tin toàn cầu của AWS, cho phép bạn gửi thông báo từ hệ thống đến người dùng qua email, SMS hoặc đến các hệ thống khác.

Lợi ích: SNS giúp đảm bảo rằng thông báo và thông tin quan trọng được gửi đi nhanh chóng và hiệu quả, hỗ trợ việc theo dõi và quản lý hoạt động của ứng dụng.

### Liên kết tham khảo

- [API Gateway REST APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-rest-api.html)
- [Building Lambda functions with Python](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html)
- [Working with tables and data in DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html)
- [Amazon Cognito - Control access to REST APIs using Amazon Cognito user pools as an authorizer](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.html)
- [How to use Amazon SNS with AWS Lambda Function](https://medium.com/cloudnloud/how-to-use-aws-lambda-function-with-amazon-sns-e8fe38097725)
