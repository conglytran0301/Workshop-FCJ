+++
title = "Thiết lập cấu hình CORS"
date = 2020-05-14T00:38:32+07:00
weight = 5
chapter = false
pre = "<b>8.5 </b>"
+++

#### Thiết lập cấu hình CORS

1. Trong giao diện **API**

   - Chọn **Resources**
   - Chọn **/serverless**
   - Chọn **Enable CORS**
     ![16-API](/images/9/9-api-16.png?width=90pc)

2. Trong giao diện **Enable CORS**

   - **Gateway responses** chọn **Default 4XX** và **Default 5XX**
   - **Access-Control-Allow-Methods** chọn **GET**
   - **Access-Control-Allow-Headers** nhập thêm `Authorization` vào cuối dòng
   - Chọn **Save**
     ![17-API](/images/9/9-api-17.png?width=90pc)
