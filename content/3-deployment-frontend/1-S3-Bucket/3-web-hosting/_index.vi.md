+++
title = "Bật Static website hosting"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3.1.3 </b>"
+++

#### Bật Static website hosting

1. Vào **S3 bucket** đã tạo

   - Chọn **Properties**
     ![13-S3](/images/3/3-s3-13.png?width=90pc)

2. Trong giao diện **Properties**

   - Kéo xuống tìm **_Static website hosting_** và chọn **Edit**
     ![14-S3](/images/3/3-s3-14.png?width=90pc)

3. Trong giao diện **Edit static website hosting**

   - Ở mục **Static website hosting**, chọn **Enable**
   - Ở mục **Hosting type**, chọn **Host a static website**
   - Ở mục **Index document**, nhập `index.html`
   - Ở mục **Error document**, nhập `error.html`
     ![15-S3](/images/3/3-s3-15.png?width=90pc)

   - Kéo xuống và chọn **Save changes**
     ![16-S3](/images/3/3-s3-16.png?width=90pc)
