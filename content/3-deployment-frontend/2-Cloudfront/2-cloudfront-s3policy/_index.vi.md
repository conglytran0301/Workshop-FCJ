+++
title = "Cloudfront Origin request policy"
date = 2020-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2.2.2 </b>"
+++

#### Cloudfront Origin request policy

1. Ở giao diện **Distributions**

   - Chọn **Distributions** bạn vừa tạo
     ![09-Cloudfront](/images/4/4-cloudfront-09.png?width=90pc)

   - Chọn **Origins**
   - Chọn **Origin name** bạn vừa tạo
   - Chọn **Edit**
     ![10-Cloudfront](/images/4/4-cloudfront-10.png?width=90pc)

2. Ở giao diện **Edit origin**

   - Chọn **OAC** vừa tạo.
   - Chọn **Copy policy**
   - Chuyển hướng đến **S3 bucket** bạn đã tạo
     ![05-Cloudfront](/images/4/4-cloudfront-05.png?width=90pc)

   - Sau khi vào **Bucket** của bạn, chọn **Permissions**
     ![12-Cloudfront](/images/4/4-cloudfront-12.png?width=90pc)

   - Kéo xuống tìm **Bucket policy**, chọn **Edit**
     ![13-Cloudfront](/images/4/4-cloudfront-13.png?width=90pc)

   - Dán mã vào **Bucket policy** của S3
   - Chọn **Save changes**
     ![14-Cloudfront](/images/4/4-cloudfront-14.png?width=90pc)

   - Bạn đã tạo thành công **Origin request policy**
