+++
title = "Triển khai Web Front-end"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

Web frontend trong kiến trúc này là phần giao diện người dùng của ứng dụng, được triển khai và quản lý trên các dịch vụ của AWS để đảm bảo tính hiệu quả và an toàn. Nội dung tĩnh của frontend, bao gồm HTML, CSS, và JavaScript, được lưu trữ trên dịch vụ lưu trữ đối tượng, sau đó được phân phối đến người dùng thông qua mạng phân phối nội dung (CDN). Điều này giúp đảm bảo trang web tải nhanh và hoạt động ổn định trên toàn cầu. Để bảo mật, frontend được bảo vệ bởi tường lửa ứng dụng web (WAF) và sử dụng chứng chỉ SSL/TLS, được quản lý thông qua các dịch vụ của AWS, đảm bảo dữ liệu người dùng được mã hóa và an toàn. Ngoài ra, hệ thống DNS của AWS được cấu hình để điều hướng tên miền đến các tài nguyên cần thiết, tạo nên một kiến trúc web frontend mạnh mẽ và an toàn.

### Nội dung

1. [Khởi tạo S3 Bucket](3-deployment-frontend/1-S3-Bucket)
2. [Cấu hình Cloudfront](3-deployment-frontend/2-Cloudfront)
3. [Cấu hình Route 53 và Certificate Manager](3-deployment-frontend/3-Route53-ACM)
4. [Khởi tạo WAF](3-deployment-frontend/4-WAF)

#### Tài liệu tham khảo

- [Uploading objects - Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html)
- [Improve Your Architecture With Amazon CloudFront](https://catalog.us-east-1.prod.workshops.aws/workshops/4557215e-2a5c-4522-a69b-8d058aba088c/en-US/basic-configuration)
- [Tutorials - Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Tutorials.html)
- [DNS validation - AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/dns-validation.html)
- [Use AWS WAF protections](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-awswaf.html)
