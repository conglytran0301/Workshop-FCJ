+++
title = "Tạo S3 bucket"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>3.1.1 </b>"
+++

#### Tạo S3 bucket

1.  Truy cập vào
    [AWS Management Console](https://ap-southeast-1.console.aws.amazon.com/console/home?region=ap-southeast-1#)

    - Tìm **S3**
    - Chọn **S3**
      ![01-S3](/images/3/3-s3-01.png?width=90pc)

2.  Trong giao diện **S3**

    - Chọn **Buckets**
    - Chọn **Create bucket**
      ![02-S3](/images/3/3-s3-02.png?width=90pc)

3.  Trong giao diện **Create bucket**

    - **Bucket name**, nhập `s3-workshop-fcj`
    - Ở phần **Object Ownership**, chọn **ACLs disabled**
      ![03-S3](/images/3/3-s3-03.png?width=90pc)

    {{% notice info %}}
    Lưu ý: Vì **Bucket name** là duy nhất trên mức độ toàn cầu, nếu đặt trùng tên với nhau thì sẽ xuất hiện thông báo: _**“Bucket with the same name already exists”**_. Do đó, cần thêm vài số phía sau để Bucket name của bạn phù hợp với policy.
    {{% /notice %}}

        ![04-S3](/images/3/3-s3-04.png?width=90pc)

    - Ở phần **Block Public Access settings for this bucket**, giữ nguyên mặc định
      ![05-S3](/images/3/3-s3-05.png?width=90pc)

    - Các phần còn lại giữ nguyên mặc định. Cuộn xuống và chọn **Create bucket**
      ![06-S3](/images/3/3-s3-06.png?width=90pc)

4.  Hoàn thành tạo **S3 bucket** để lưu trữ _source website_
    ![07-S3](/images/3/3-s3-07.png?width=90pc)
