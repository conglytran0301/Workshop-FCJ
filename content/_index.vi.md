+++
title = "AWS Serverless web app"
date = 2024
weight = 1
chapter = false
+++

# Serverless Web Application Building on AWS

#### Tổng quan

Trong bài này, chúng ta sẽ xây dựng một hệ thống ứng dụng Web sử dụng các dịch vụ **Serverless** trên nền tảng AWS. Hệ thống này tận dụng các dịch vụ như **S3** để lưu trữ nội dung tĩnh, **API Gateway** để quản lý và định tuyến yêu cầu API, **Lambda** để xử lý logic nghiệp vụ, và **DynamoDB** để lưu trữ dữ liệu động. Các dịch vụ bổ sung như **Route53**, **CloudFront**, và **WAF** giúp bảo đảm hiệu suất cao và an ninh cho ứng dụng. Ngoài ra, **Cognito** được sử dụng để quản lý xác thực người dùng, và **SNS** giúp gửi thông báo tức thì. Tổng thể, kiến trúc này mang lại sự linh hoạt, khả năng mở rộng, và hiệu quả chi phí, đồng thời tối ưu hóa trải nghiệm người dùng và bảo mật hệ thống.

![Serverless-FCJ](/images/1-account-setup/Serverles.png?width=90pc)

#### Nội dung

1. [Giới thiệu](1-introduction/)
2. [Các bước chuẩn bị](2-preparation>)
3. [Triển khai Web Front-end](3-deployment-frontend/)
4. [Khởi tạo SNS](4-sns/)
5. [Khởi tạo Cognito](5-cognito/)
6. [Khởi tạo DynamoDB](6-dynamodb/)
7. [Triển khai Lambda function](7-lambda-function/)
8. [Thiết lập API Gateway](8-api-gateway/)
9. [Kiểm tra Web Application](9-test-webapp/)
10. [Dọn dẹp tài nguyên](10-clean-resource/)
