+++
title = "Khởi tạo Cognito User pool"
date = 2024-08-19T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++

#### Khởi tạo Cognito User pool

1. Truy cập vào
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Tìm **Cognito**
   - Chọn **Cognito**
     ![01-Cognito](/images/6/6-cognito-01.png?width=90pc)

2. Trong giao diện **Cognito**

   - Chọn **Create user pool**
     ![02-Cognito](/images/6/6-cognito-02.png?width=90pc)

3. Trong giao diện **Create user pool**

   Ở Step 1 **Configure sign-in experience**

   - Tìm **Cognito user pool sign-in options**, chọn **User name** và **Email**
   - Chọn **Next**
     ![03-Cognito](/images/6/6-cognito-03.png?width=90pc)

   Ở Step 2 **Configure security requirements**

   - **Password policy mode** chọn **Cognito defaults**
     ![04-Cognito](/images/6/6-cognito-04.png?width=90pc)

   - **Multi-factor authentication** chọn **No MFA**
   - **Self-service account recovery** chọn **Enable self-service account recovery - Recommended**
   - **Delivery method for user account recovery messages** chọn **Email only**
   - Chọn **Next**
     ![05-Cognito](/images/6/6-cognito-05.png?width=90pc)

   Ở Step 3 **Configure sign-up experience**

   - Tất cả để **mặc định**
   - Chọn **Next**
     ![07-Cognito](/images/6/6-cognito-07.png?width=90pc)

   Ở Step 4 **Configure message delivery**

   - **Email** chọn **Send email with Cognito**
   - **FROM email address** chọn **no-reply@verificationemail.com**
   - Chọn **Next**
     ![06-Cognito](/images/6/6-cognito-06.png?width=90pc)

   Ở Step 5 **Integrate your app**

   - **User pool name** nhập `FCJUserPool`
   - Chọn **Use the Cognito Hosted UI**
   - **Domain type** chọn **Use a Cognito domain**
   - **Cognito domain** nhập **tên miền đăng nhập Cognito mà bạn muốn**
     ![08-Cognito](/images/6/6-cognito-08.png?width=90pc)

   - **App type** chọn **Public client**
   - **App client name** nhập `FCJ-Client`
   - **Allowed callback URLs** nhập **http://'tên miền đã gán cho web của bạn'/contact-me.html**

   {{% notice note %}}Giao diện web thứ 1 là **/index.html** và giao diện web thứ 2 là **/contact-me.html**. Khi điền **Allowed callback URLs** phải có **/contact-me.html** ở phía sau tên miền của bạn, để từ giao diện của **/index.html** có thể **callback** sang **/contact-me.html**.
   {{% /notice %}}
   ![12-Cognito](/images/6/6-cognito-12.png?width=90pc)

   - Kéo xuống tìm **Advanced app client settings**
   - **OAuth 2.0 grant types**, bỏ chọn **Authorization code grant** và chọn **Implicit grant**
   - **OpenID Connect scopes** chọn **OpenID**, **Phone**, **Email**, **aws.cognito.signin.user.admin**, **Profile**
   - **Allowed sign-out URLs - optional** nhập **http://'tên miền đã gán cho web của bạn'/index.html**
     ![13-Cognito](/images/6/6-cognito-13.png?width=90pc)

   - Kéo xuống và chọn **Next**

   Ở Step 6 **Review and create**

   - Kiểm tra lại và chọn **Create user pool**
     ![10-Cognito](/images/6/6-cognito-10.png?width=90pc)
