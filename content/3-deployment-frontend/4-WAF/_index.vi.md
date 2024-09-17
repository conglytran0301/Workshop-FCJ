+++
title = "Khởi tạo WAF"
date = 2020-05-14T00:38:32+07:00
weight = 4
chapter = false
pre = "<b>3.4 </b>"
+++

#### Khởi tạo WAF

{{% notice note %}}
Khi tạo 1 **Web ACL** thì các bạn sẽ mất 5$ cho 1 tháng sử dụng.
{{% /notice %}}

1. Truy cập vào
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Tìm **WAF**
   - Chọn **WAF**
     ![01-WAF](/images/3/3-waf-01.png?width=90pc)

2. Trong giao diện **WAF**

   - Chọn **Create web ACL**
     ![02-WAF](/images/3/3-waf-02.png?width=90pc)

3. Trong giao diện **Create web ACL**

   Step 1 **Describe web ACL and associate it to AWS resources**

   - **Resource type** chọn **Amazon CloudFront distributions**
   - **Name** nhập `WAF-Demo`
     ![03-WAF](/images/3/3-waf-03.png?width=90pc)

   - **Associated AWS resources** chọn **Add AWS resources**
     ![04-WAF](/images/3/3-waf-04.png?width=90pc)

   - Chọn tên miền bạn đã đăng kí cho **Cloudfront**
   - Sau đó chọn **Add**
     ![05-WAF](/images/3/3-waf-05.png?width=90pc)

   - **CloudFront distributions** chọn **Default**
   - Chọn **Next**
     ![06-WAF](/images/3/3-waf-06.png?width=90pc)

   Step 2 **Add rules and rule groups**

   - **Rules** chọn **Add rules**
   - Chọn **Add managed rule groups**
     ![07-WAF](/images/3/3-waf-07.png?width=90pc)

   - Chọn **AWS managed rule groups**
     ![08-WAF](/images/3/3-waf-08.png?width=90pc)

   - Tìm phần **Free rule groups**
   - **Amazon IP reputation list** chọn **Add to web ACL**
     ![09-WAF](/images/3/3-waf-09.png?width=90pc)

   - Kéo xuống và chọn **Add rules**
     ![10-WAF](/images/3/3-waf-10.png?width=90pc)

   - **Default action** chọn **Allow**
   - Chọn **Next**
     ![11-WAF](/images/3/3-waf-11.png?width=90pc)

   Step 3 **Set rule priority**

   - Chọn **Next**
     ![12-WAF](/images/3/3-waf-12.png?width=90pc)

   Step 4 **Configure metrics**

   - Chọn **Next**
     ![13-WAF](/images/3/3-waf-13.png?width=90pc)

   - Kiểm tra lại và chọn **Create web ACL**
     ![14-WAF](/images/3/3-waf-14.png?width=90pc)
