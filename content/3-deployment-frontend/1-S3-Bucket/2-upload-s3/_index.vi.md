+++
title = "Upload dữ liệu"
date = 2020-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>3.1.2 </b>"
+++

#### Upload dữ liệu

{{% notice note %}}
Chúng ta sẽ upload _source code_ lên **S3 bucket** để lưu trữ. Nếu bạn chưa tải _source code_ về máy, quay lại phần [2.1.Clone repository từ Github](2-preparation/1-clone-code) để clone repo.
{{% /notice %}}

1. Trong giao diện **S3 bucket** vừa tạo

- Hiện tại vẫn chưa có **Object** trong **Bucket**
- Chọn **Upload** để tải dữ liệu lên

![08-S3](/images/3/3-s3-08.png?width=90pc)

2. Trong giao diện **Upload**

- Vào **Folder** có tên _**FCJ-Serverless**_ đã được _clone_ từ **Github** ở bước trên
- Nhấn tổ hợp phím **CRLT + A** để chọn tất cả thư mục
- Sau đó kéo toàn bộ Folder và File và thả vào giao diện **Upload** của **S3 bucket**.

![09-S3](/images/3/3-s3-09.png?width=90pc)

- Sau khi đã chọn tất cả thư mục thả vào **Bucket**

![10-S3](/images/3/3-s3-10.png?width=90pc)

- Cuộn xuống cuối trang và Chọn **Upload**

![11-S3](/images/3/3-s3-11.png?width=90pc)

- Sau khi **Upload** hoàn thành, bạn sẽ thấy các tệp đã được thêm vào **S3 Bucket**

![12-S3](/images/3/3-s3-12.png?width=90pc)
