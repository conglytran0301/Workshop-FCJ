+++
title = "Cấu hình Route 53 và Certificate Manager"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3.3 </b>"
+++

#### Cấu hình Route 53

1. Truy cập vào [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

- Tìm **Route 53**
- Chọn **Route 53**

![01-Route53-ACM](/images/3/3-route53-acm-01.png?width=90pc)

2. Trong giao diện **Route 53**

- Chọn **Hosted zones**
- Chọn **Create hosted zone**

![02-Route53-ACM](/images/3/3-route53-acm-02.png?width=90pc)

3. Trong giao diện **Create hosted zone**

- Viết **Domain name** đã đăng ký ở bài trước
- Ở phần **Type**, chọn **Public hosted zone**
- Chọn **Create hosted zone**

![03-Route53-ACM](/images/3/3-route53-acm-03.png?width=90pc)

4. Quay lại giao diện **Hosted zones**

- Vào **Hosted zone name** vừa tạo

![04-Route53-ACM](/images/3/3-route53-acm-04.png?width=90pc)

- Chọn **Create record**

![05-Route53-ACM](/images/3/3-route53-acm-05.png?width=90pc)

5. Trong giao diện **Create record**

- **Record type** chọn **CNAME**
- **Record name** nhập `workshop`
- **Value** nhập **Distribution domain name** của **Cloudfront** (Ví dụ: `https://d23akwur3rh4c.cloudfront.net`)
- Chọn **Create records**

![06-Route53-ACM](/images/3/3-route53-acm-06.png?width=90pc)

#### Cấu hình Certificate Manager

1. Truy cập vào [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

- Tìm `Certificate Manager`
- Chọn **Certificate Manager**

![08-Route53-ACM](/images/3/3-route53-acm-08.png?width=90pc)

2. Trong giao diện **Certificate Manager**

- Chuyển **Region** sang **N.Virginia**

![07-Route53-ACM](/images/3/3-route53-acm-07.png?width=90pc)

- Chọn **Request certificate**
- **Certificate type** chọn **Request a public certificate**
- Chọn **Next**

![09-Route53-ACM](/images/3/3-route53-acm-09.png?width=90pc)

- Trong phần **Request public certificate**
- **Domain names** nhập **workshop.conglyblog.id.vn**

![10-Route53-ACM](/images/3/3-route53-acm-10.png?width=90pc)

- Các phần còn lại giữ mặc định
- Kéo xuống và chọn **Request**

![11-Route53-ACM](/images/3/3-route53-acm-11.png?width=90pc)

3. Sau khi **Request** thành công

- Tìm mục **Domains**
- Chọn **Create records in Route 53**

![12-Route53-ACM](/images/3/3-route53-acm-12.png?width=90pc)

- Lúc này **records** đã được tạo

![14-Route53-ACM](/images/3/3-route53-acm-14.png?width=90pc)

- Vào **Route 53** kiểm tra lại

![13-Route53-ACM](/images/3/3-route53-acm-13.png?width=90pc)

- Chúc mừng, bạn đã tạo **Certificate** cho tên miền thành công.
