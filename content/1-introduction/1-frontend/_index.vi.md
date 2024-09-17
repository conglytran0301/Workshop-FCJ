+++
title = "Định tuyến, Phân phối Nội dung và Bảo mật"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1.1 </b>"
+++

### Tổng quan

**1. Route53:** là dịch vụ DNS (Domain Name System) có khả năng mở rộng cao của AWS. Nó giúp chuyển đổi các tên miền dễ nhớ mà người dùng nhập vào trình duyệt thành địa chỉ IP của tài nguyên AWS.

Lợi ích: Route 53 đảm bảo việc định tuyến lưu lượng đến đúng tài nguyên AWS với độ tin cậy và tốc độ cao. Nó cũng cung cấp tính năng quản lý DNS, kiểm tra sức khỏe, và định tuyến dựa trên địa lý, giúp tối ưu hóa trải nghiệm người dùng toàn cầu.

**2. CloudFront:** là mạng phân phối nội dung (CDN) của AWS, giúp phân phối các nội dung tĩnh như hình ảnh, video, và tài liệu từ các máy chủ gần người dùng nhất.

Lợi ích: CloudFront giảm thiểu độ trễ và tăng tốc độ tải trang web nhờ vào các edge location trên toàn cầu. Nó cũng tích hợp với các dịch vụ bảo mật của AWS như AWS WAF và AWS Shield để bảo vệ nội dung khỏi các mối đe dọa trực tuyến.

**3. S3 (Simple Storage Service):** là dịch vụ lưu trữ đối tượng có khả năng mở rộng cao của AWS, được thiết kế để lưu trữ và truy xuất bất kỳ lượng dữ liệu nào từ bất kỳ đâu trên web.

Lợi ích: S3 cung cấp khả năng lưu trữ đáng tin cậy, bảo mật cao với chi phí hợp lý. Bạn chỉ trả tiền cho dung lượng và lượng dữ liệu được sử dụng, giúp tối ưu hóa chi phí vận hành.

**4. WAF (Web Application Firewall):** là tường lửa ứng dụng web giúp bảo vệ các ứng dụng web khỏi các cuộc tấn công phổ biến như SQL injection và cross-site scripting (XSS).

Lợi ích: WAF cho phép bạn tạo ra các quy tắc bảo mật tùy chỉnh để bảo vệ ứng dụng của mình, đồng thời cung cấp khả năng giám sát lưu lượng và ngăn chặn các mối đe dọa trước khi chúng có thể gây ra thiệt hại.

**5. AWS Certificate Manager:** giúp quản lý chứng chỉ SSL/TLS dễ dàng hơn, từ việc cấp phát, gia hạn cho đến triển khai chúng trên các dịch vụ AWS khác như CloudFront.

Lợi ích: Việc quản lý chứng chỉ SSL/TLS một cách tự động giúp bảo mật giao tiếp giữa người dùng và ứng dụng của bạn mà không cần phải lo lắng về việc gia hạn hoặc cấu hình thủ công các chứng chỉ.

### Tài liệu tham khảo

- [Tutorials - Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Tutorials.html)
- [Improve Your Architecture With Amazon CloudFront](https://catalog.us-east-1.prod.workshops.aws/workshops/4557215e-2a5c-4522-a69b-8d058aba088c/en-US/basic-configuration)
- [Uploading objects - Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html)
- [Use AWS WAF protections](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-awswaf.html)
- [DNS validation - AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/dns-validation.html)
