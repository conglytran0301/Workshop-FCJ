+++
title = "Khởi tạo SNS"
date = 2024-08-19T00:38:32+07:00
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

#### Khởi tạo SNS

1. Truy cập vào
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Tìm **SNS**
   - Chọn **Simple Notification Servicet**
     ![01-SNS](/images/5/5-sns-01.png?width=90pc)

2. Trong giao diện của **SNS**

   - Ở phần **Create topic**, nhập **Topic name:** `FCJ-SNSTopic`
   - Chọn **Next step**
     ![02-SNS](/images/5/5-sns-02.png?width=90pc)

3. Trong giao diện của **Create topic**

   - Ở phần **Type** chọn **Standard**
     ![03-SNS](/images/5/5-sns-03.png?width=90pc)

   - Các phần còn lại giữ mặc định
   - Kéo xuống cuối trang và chọn **Create topic**
     ![04-SNS](/images/5/5-sns-04.png?width=90pc)

   - Sau khi tạo **Topic**, chọn **Subscriptions** ở thanh bên trái
   - Chọn **Create subscription**
     ![05-SNS](/images/5/5-sns-05.png?width=90pc)

4. Trong giao diện **Create subscription**

   - Ở phần **Topic ARN**, chọn **Topic** bạn vừa tạo
   - **Protocol** chọn **Email**
   - **Endpoint** nhập **email cá nhân** của bạn
   - Sau đó chọn **Create subscription**
     ![07-SNS](/images/5/5-sns-07.png?width=90pc)

5. Sau khi **Create subscription**

   - Vào **email** bạn đã nhập khi tạo **subscription**
   - Chọn **Confirm subscription** để xác nhận đăng ký
     ![08-SNS](/images/5/5-sns-08.png?width=90pc)

   - Bạn đã hoàn thành **Confirm subscription**

   {{% notice note %}}Sau khi chọn **Confirm subscription** bạn chỉ cần thoát ra là hoàn thành. (Nếu chọn **click here to unsubcribe** bạn sẽ hủy đăng ký và không thể nhận thông tin về **email**).
   {{% /notice %}}
   ![09-SNS](/images/5/5-sns-09.png?width=90pc)
