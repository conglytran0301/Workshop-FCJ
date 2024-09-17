+++
title = "Tạo Authorizer"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>8.3 </b>"
+++

#### Tạo Authorizer

1. Trong gia diện **API**

   - Chọn **Authorizers**
   - Chọn **Create authorizer**
     ![10-API](/images/9/9-api-10.png?width=90pc)

2. Trong giao diện **Create authorizer**

   - **Authorizer name** nhập `FCJ-Auth`
   - **Authorizer type** chọn **Cognito**
   - **Cognito user pool** chọn **FCJ-UserPool**
   - **Token source** nhập `Authorization`
   - Chọn **Create authorizer**
     ![11-API](/images/9/9-api-11.png?width=90pc)

3. Vào giao diện **Resources**

   - Chọn **GET**
   - Chọn **Method request**
   - Chọn **Edit**
     ![12-API](/images/9/9-api-12.png?width=90pc)

4. Trong giao diện **Edit method request**

   - **Authorization** chọn **FCJ-Auth**
   - **Authorization scopes** nhập `email`, sau đó chọn **add**
   - Kéo xuống và chọn **Save**
     ![13-API](/images/9/9-api-13.png?width=90pc)
