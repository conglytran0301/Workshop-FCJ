+++
title = "Kiểm tra Cognito User pool"
date = 2024-08-19T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>5.2 </b>"
+++

#### Kiểm tra Cognito User pool

1. Trong giao diện **User pool**

   - Chọn **User pool** mà bạn vừa tạo
     ![14-Cognito](/images/6/6-cognito-14.png?width=90pc)

   - Chọn **App integration**
     ![15-Cognito](/images/6/6-cognito-15.png?width=90pc)

   - Kéo xuống phần **App clients and analytics**
   - Chọn **App client name** bạn đã tạo
     ![16-Cognito](/images/6/6-cognito-16.png?width=90pc)

   - Kéo xuống phần **Hosted UI**
   - Chọn **View Hosted UI**
     ![17-Cognito](/images/6/6-cognito-17.png?width=90pc)

   {{% notice note %}}Bạn đã mở được trang đăng ký tài khoản của **Cognito**, nhưng vẫn chưa vào được giao diện thứ 1 (/index.html). Để vào được giao diện này, bạn cần thêm _link URL_ của **Cognito** vào **code website** của bạn.
   {{% /notice %}}

2. Trong giao diện Login của **Cognito**

   - Chọn **copy** đường dẫn trên trang đăng nhập của **Cognito**
     ![26-Cognito](/images/6/6-cognito-26.png?width=90pc)

   - Mở **code** bạn đã clone
   - Chọn file **index.html**. Tìm dòng 'Change - Sign in Link' và dán đường dẫn vào.
     ![30-Cognito](/images/6/6-cognito-30.png?width=90pc)

   - Tiếp theo chọn file **contact-me.html**. Tìm dòng 'Change - SignOut URL' và dán đường dẫn cũ vào.
     ![29-Cognito](/images/6/6-cognito-29.png?width=90pc)

   ```
   //Đường dẫn SignIn và SignOut có cấu trúc như sau:

   MAKE URL OF SIGN IN /login?client_id=&response_type=token&scope=aws.cognito.signin.user.admin+email+openid+phone+profile&redirect_uri=

   MAKE URL OF SIGN OUT /logout?client_id=&response_type=token&scope=aws.cognito.signin.user.admin+email+openid+phone+profile&redirect_uri=
   ```

   - Sau đó vào file **main.js**
   - Tìm **window.location.href** và dán tên miền có đuôi `/index.html` của bạn.
     ![28-Cognito](/images/6/6-cognito-28.png?width=90pc)

   - Cuối cùng update lại trên S3 của bạn.

3. Quay lại giao diện trang web

   - Sau khi đã update trên S3, bạn quay lại giao diện **Hosted UI**
   - Chọn **View Hosted UI**
   - Lúc này, bạn đã vào được trang web thứ 1
   - Chọn **LOGIN**
     ![18-Cognito](/images/6/6-cognito-18.png?width=90pc)

   - Chọn **Sign up** để đăng kí tài khoản
     ![19-Cognito](/images/6/6-cognito-19.png?width=90pc)

   - **Username** nhập '_Username của bạn_'
   - **Email** nhập '_Email của bạn_'
   - **Password** nhập '_Password của bạn_'
     ![20-Cognito](/images/6/6-cognito-20.png?width=90pc)

   - Vào **Email** bạn vừa đăng ký để lấy **code**
     ![21-Cognito](/images/6/6-cognito-21.png?width=90pc)

   - **Code** đã được gửi vào **Email** của bạn
     ![22-Cognito](/images/6/6-cognito-22.png?width=90pc)

   - Copy **code** và dán vào ô của **Verification code**
   - Sau đó chọn **Confirm account**
     ![23-Cognito](/images/6/6-cognito-23.png?width=90pc)

   - Chúc mừng, bạn đã đăng ký tài khoản thành công và vào được giao diện thứ 2
     ![25-Cognito](/images/6/6-cognito-25.png?width=90pc)
