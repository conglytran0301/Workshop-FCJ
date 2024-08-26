+++
title = "Đăng ký tên miền"
date = 2020-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2.2 </b>"
+++

#### Đăng kí tên miền với Amazon Route 53

1. Truy cập vào [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

- Tìm **Route 53**
- Chọn **Route 53**

![01-Route53](/images/2/2-03-domain.png?width=90pc)

2. Trong giao diện **Route 53**

- Chọn **Registered domains**

![02-Route53](/images/2/2-04-domain.png?width=90pc)

3. Trong giao diện **Registered domains**

- Nhập tên miển muốn đăng ký
- Chọn **Search**
- Ấn **Select** tên miền muốn đăng ký
- Chọn **Proceed to checkout**

![02-Route53](/images/2/2-05-domain.png?width=90pc)

4. Trong phần **Pricing**

- Lựa chọn thời gian đăng kí và gia hạn
- Chọn **Next**

![03-Route53](/images/2/2-06-domain.png?width=90pc)

5. Trong phần **Contact information**

- Điền thông tin liên hệ
- Chọn **Next**

![04-Route53](/images/2/2-07-domain.png?width=90pc)

6. Trong phần **Review and submit**

- Kiểm tra lại thông tin
- Chọn **Submit**

![05-Route53](/images/2/2-08-domain.png?width=90pc)

7. Kiểm tra tên miền

- Vào **Registered domains** để kiểm tra thông tin tên miền đã đăng ký.

![06-Route53](/images/2/2-09-domain.png?width=90pc)

{{% notice info %}}
Nếu bạn đăng kí tên miền thất bại, vui lòng liên hệ với [**AWS Support**](https://support.console.aws.amazon.com/) để được hỗ trợ.
{{% /notice %}}

#### Đăng kí tên miền với domain provider khác

1. Vào **Console** của **domain provider** bạn đã mua

- Chọn **Quản lí tên miền**
- Chọn **tên miền** mà bạn **đã đăng ký**

![10-Route53](/images/2/2-10-domain.png?width=90pc)

- Chọn **Name Server**
- Nhập **Name Server** được cung cấp trong **Hosted zones** của**Route53**

![11-Route53](/images/2/2-11-domain.png?width=90pc)

{{% notice note %}}
Để có thể tạo DNS từ **domain provider khác** sang **AWS**, bạn cần tạo **Hosted zones** trong **Route 53**. Sau đó nhập **Name Server** được **Route 53** cung cấp vào phần nhập **Name Server** của **domain provider khác**. _Các bước đăng ký **Hosted zones** bạn xem hướng dẫn ở đây_: "[Cấu hình Route 53 và Certificate Manager](3-deployment-frontend/3-Route53-ACM)". **Lưu ý: Quá trình thay đổi có thể cần đến 24 giờ để có hiệu lực.**
{{% /notice %}}
