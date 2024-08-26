+++
title = "Tạo Cloudfront"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>2.2.1 </b>"
+++

#### Tạo Cloudfront

1. Truy cập vào [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

- Tìm **Cloudfront**
- Chọn **Cloudfront**

![01-Cloudfront](/images/4/4-cloudfront-01.png?width=90pc)

2. Trong giao diện **Cloudfront**

- Chọn **Distributions**
- Chọn **Create distribution**

![02-Cloudfront](/images/4/4-cloudfront-02.png?width=90pc)

3. Trong giao diện **Create distribution**

- **Origin domain**, chọn tên **S3 bucket** đã tạo
- **Origin access**, chọn **Origin access control settings (recommended)**
- **Origin access control**, chọn **Create new OAC**

![03-Cloudfront](/images/4/4-cloudfront-03.png?width=90pc)

- Trong giao diện **Create new OAC**, để mặc định. Sau đó chọn **Create**

![04-Cloudfront](/images/4/4-cloudfront-04.png?width=90pc)

- Sau khi **Create new OAC**, chọn OAC vừa tạo

![15-Cloudfront](/images/4/4-cloudfront-15.png?width=90pc)

- Kéo xuống phần **Viewer protocol policy**, chọn **Redirect HTTP to HTTPS**
- Ở phần **Allowed HTTP methods**, chọn **GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE**

![06-Cloudfront](/images/4/4-cloudfront-06.png?width=90pc)

- Ở phần **Web Application Firewall (WAF)**, chọn **Do not enable security protections**

![07-Cloudfront](/images/4/4-cloudfront-07.png?width=90pc)

- Các phần còn lại để mặc định. Kéo xuống và chọn **Create distribution**

![08-Cloudfront](/images/4/4-cloudfront-08.png?width=90pc)

- Chúc mừng bạn đã tạo thành công **Distribution**
- Quá trình khởi tạo sẽ mất 4-5 phút để hoàn thành.
