+++
title = "Serverless Web Application Building on AWS"
date = 2024
weight = 1
chapter = false
+++

# Serverless Web Application Building on AWS

### Tổng quan về Workshop

#### Kiến trúc Serverless của Workshop

![Serverless-FCJ](/images/1/Serverles.png?width=90pc)

#### Mục tiêu của Workshop

Workshop "Serverless Web Application Building on AWS" có mục tiêu chính là giúp người tham gia hiểu rõ cách xây dựng một kiến trúc serverless trên AWS với các dịch vụ tích hợp, đảm bảo tối ưu hóa chi phí, bảo mật, và khả năng mở rộng.

#### Kiến thức được cung cấp trong Workshop

**Các dịch vụ AWS và chi phí:**

1.  **Amazon Route 53**: Là dịch vụ DNS (Domain Name System) có khả năng mở rộng cao của AWS. Nó giúp chuyển đổi các tên miền dễ nhớ mà người dùng nhập vào trình duyệt thành địa chỉ IP của tài nguyên AWS.

    - Chức năng: Route 53 đảm bảo việc định tuyến lưu lượng đến đúng tài nguyên AWS với độ tin cậy và tốc độ cao. Nó cũng cung cấp tính năng quản lý DNS, kiểm tra sức khỏe, và định tuyến dựa trên địa lý, giúp tối ưu hóa trải nghiệm người dùng toàn cầu.
    - Free Tier: 1 triệu truy vấn DNS tiêu chuẩn miễn phí hàng tháng.

      **_Giá tiêu chuẩn:_**

      - $0.50/tháng cho mỗi miền được quản lý.
      - $0.40 cho mỗi triệu truy vấn tiếp theo (ngoài 1 triệu miễn phí).

2.  **AWS CloudFront**: Là mạng phân phối nội dung (CDN) của AWS, giúp phân phối các nội dung tĩnh như hình ảnh, video, và tài liệu từ các máy chủ gần người dùng nhất.

    - Chức năng: Giảm độ trễ, tăng tốc độ truy cập ứng dụng cho người dùng khắp thế giới. Nó cũng tích hợp với các dịch vụ bảo mật của AWS như AWS WAF và AWS Shield để bảo vệ nội dung khỏi các mối đe dọa trực tuyến.
    - Free Tier: 1 TB dữ liệu truyền tải và 2 triệu yêu cầu HTTP/HTTPS miễn phí trong 12 tháng đầu.

      **_Giá tiêu chuẩn:_**

      - $0.085/GB cho 10 TB đầu tiên.
      - $0.0075/10.000 yêu cầu HTTP/HTTPS.

3.  **Amazon S3**: Là dịch vụ lưu trữ đối tượng có khả năng mở rộng cao của AWS, được thiết kế để lưu trữ và truy xuất bất kỳ lượng dữ liệu nào từ bất kỳ đâu trên web.

    - Chức năng: Lưu trữ và truy xuất dữ liệu. S3 cung cấp khả năng lưu trữ đáng tin cậy, bảo mật cao với chi phí hợp lý. Bạn chỉ trả tiền cho dung lượng và lượng dữ liệu được sử dụng, giúp tối ưu hóa chi phí vận hành.
    - Tối ưu hóa chi phí: Lưu trữ nhiều lớp (S3 Standard, S3 Glacier) cho chi phí thấp hơn.
    - Free Tier: 5 GB lưu trữ tiêu chuẩn (S3 Standard) miễn phí trong 12 tháng đầu tiên.

      **_Giá tiêu chuẩn:_**

      - $0.023/GB cho S3 Standard (dưới 50 TB đầu tiên mỗi tháng).
      - S3 Glacier để lưu trữ lâu dài có chi phí thấp hơn, khoảng $0.004/GB mỗi tháng.

4.  **AWS WAF (Web Application Firewall)**: Là tường lửa ứng dụng web giúp bảo vệ các ứng dụng web khỏi các cuộc tấn công phổ biến như SQL injection và cross-site scripting (XSS).

    - Chức năng: Chặn các yêu cầu độc hại trước khi đến ứng dụng. WAF cho phép bạn tạo ra các quy tắc bảo mật tùy chỉnh để bảo vệ ứng dụng của mình, đồng thời cung cấp khả năng giám sát lưu lượng và ngăn chặn các mối đe dọa trước khi chúng có thể gây ra thiệt hại.

      **_Giá tiêu chuẩn:_**

      - $5.00/tháng cho mỗi Web ACL (Access Control List).
      - $0.60 cho mỗi triệu yêu cầu được đánh giá bởi ACL.

5.  **AWS Certificate Manager**: Giúp quản lý chứng chỉ SSL/TLS dễ dàng hơn, từ việc cấp phát, gia hạn cho đến triển khai chúng trên các dịch vụ AWS khác như CloudFront.

    - Chức năng: Bảo mật các kết nối giữa người dùng và CloudFront. Việc quản lý chứng chỉ SSL/TLS một cách tự động giúp bảo mật giao tiếp giữa người dùng và ứng dụng của bạn mà không cần phải lo lắng về việc gia hạn hoặc cấu hình thủ công các chứng chỉ.
    - Free Tier: Cung cấp và quản lý chứng chỉ SSL/TLS miễn phí khi sử dụng với các dịch vụ của AWS như CloudFront và Elastic Load Balancing.

      **_Giá tiêu chuẩn:_** Không có chi phí cho chứng chỉ SSL/TLS được sử dụng trong các dịch vụ AWS.

6.  **Amazon Cognito**: Cung cấp các dịch vụ quản lý người dùng và xác thực, cho phép người dùng đăng ký, đăng nhập, và truy cập các tài nguyên một cách an toàn.

    - Chức năng: Cognito giúp đơn giản hóa việc quản lý người dùng, đồng thời tích hợp với các dịch vụ AWS khác để cung cấp bảo mật toàn diện và quản lý quyền truy cập dễ dàng.
    - Free Tier: 50.000 yêu cầu xác thực người dùng mỗi tháng.

      **_Giá tiêu chuẩn:_**

      - $0.0055 cho mỗi yêu cầu xác thực vượt quá 50.000.

7.  **AWS API Gateway**: Cầu nối giữa người dùng và backend serverless (Lambda) và là dịch vụ quản lý API mạnh mẽ của AWS, giúp bạn tạo, triển khai và quản lý các API RESTful một cách dễ dàng.

    - Chức năng: Xử lý các yêu cầu API từ người dùng, xác thực và phân phối đến Lambda. API Gateway cung cấp khả năng quản lý lưu lượng, giám sát hiệu suất, và bảo mật API, giúp đảm bảo rằng ứng dụng của bạn có thể xử lý hàng triệu yêu cầu với độ tin cậy và hiệu suất cao.
    - Tối ưu hóa chi phí: Chỉ trả phí khi có yêu cầu API.
    - Free Tier: 1 triệu cuộc gọi API REST hoặc HTTP miễn phí mỗi tháng.

      **_Giá tiêu chuẩn:_**

      - $3.50 cho mỗi triệu cuộc gọi API tiếp theo.

8.  **AWS Lambda**: Nền tảng serverless chính để chạy code mà không cần quản lý máy chủ. Bạn chỉ cần cung cấp mã và Lambda sẽ tự động xử lý mọi thứ cần thiết để chạy và mở rộng mã.

    - Chức năng: Xử lý các yêu cầu được gửi từ API Gateway. Với Lambda, bạn chỉ trả tiền cho thời gian thực thi của mã, giúp tối ưu hóa chi phí và loại bỏ nhu cầu quản lý cơ sở hạ tầng. Lambda cũng tự động mở rộng quy mô để đáp ứng nhu cầu của ứng dụng.
    - Tối ưu hóa chi phí: Trả phí theo thời gian chạy và số lượng yêu cầu.
    - Free Tier: 1 triệu yêu cầu và 400.000 GB-giây thời gian tính toán mỗi tháng.

      **_Giá tiêu chuẩn:_**

      - $0.20 cho mỗi 1 triệu yêu cầu.
      - $0.00001667 cho mỗi GB-giây thời gian tính toán.

9.  **DynamoDB:** là cơ sở dữ liệu NoSQL có khả năng mở rộng cao, được thiết kế để xử lý mọi khối lượng công việc với độ trễ thấp.

    - Chức năng: DynamoDB cung cấp hiệu suất đáng tin cậy, với khả năng tự động mở rộng quy mô, giúp bạn xây dựng các ứng dụng có thể xử lý hàng triệu yêu cầu mỗi giây mà không gặp khó khăn về hiệu suất.
    - Free Tier: 25 GB dung lượng lưu trữ và 2.5 triệu yêu cầu đọc/ghi mỗi tháng trong gói miễn phí của AWS (12 tháng).

      **_Giá tiêu chuẩn:_**

      - Ghi (Write Request Units - WRU): $1.25 cho mỗi triệu yêu cầu ghi.
      - Đọc (Read Request Units - RRU): $0.25 cho mỗi triệu yêu cầu đọc.
      - Lưu trữ: $0.25/GB mỗi tháng.

10. **Amazon SNS (Simple Notification Service)**: Dịch vụ thông báo đa nền tảng, đáng tin cậy, tích hợp với các ứng dụng serverless. SNS cho phép bạn gửi thông báo từ hệ thống đến người dùng qua email, SMS hoặc đến các hệ thống khác.

    - Chức năng: Gửi thông báo qua SMS, HTTP/HTTPS, hoặc các giao thức khác tới người dùng hoặc hệ thống tự động. SNS giúp đảm bảo rằng thông báo và thông tin quan trọng được gửi đi nhanh chóng và hiệu quả, hỗ trợ việc theo dõi và quản lý hoạt động của ứng dụng.

    - Free Tier: 1 triệu yêu cầu (requests) miễn phí mỗi tháng và 1.000 thông báo SMS miễn phí khi gửi từ SNS mỗi tháng (tùy thuộc vào vùng).

      **_Giá tiêu chuẩn:_**

      - Yêu cầu gửi thông báo (request): $0.50 cho mỗi 1 triệu yêu cầu.

      - Gửi SMS: Giá SMS thay đổi theo vùng và nhà mạng (ví dụ: $0.02018 cho mỗi SMS tại Singapore).

      - HTTP/HTTPS, SQS, Lambda, Mobile Push: Không tính phí khi gửi thông báo tới các dịch vụ này.

#### Tài liệu Tham khảo về các Dịch vụ và Chi phí trong Workshop

**Tài liệu về các dịch vụ:**

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

**Tài liệu về chi phí:**

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

### Nội dung

1. [Giới thiệu](1-introduction)
2. [Các bước chuẩn bị](2-preparation)
3. [Triển khai Web Front-end](3-deployment-frontend)
4. [Khởi tạo SNS](4-sns)
5. [Khởi tạo Cognito](5-cognito)
6. [Khởi tạo DynamoDB](6-dynamodb)
7. [Triển khai Lambda function](7-lambda-function)
8. [Thiết lập API Gateway](8-api-gateway)
9. [Kiểm tra Web Application](9-test-webapp)
10. [Dọn dẹp tài nguyên](10-clean-resource)
