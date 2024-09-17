+++
title = "Dọn dẹp tài nguyên"
date = 2024-08-19T00:38:32+07:00
weight = 10
chapter = false
pre = "<b>10. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa S3

1. Truy cập vào giao diện của **S3**
2. Chọn **Buckets**
3. Chọn **Bucket name** bạn đã tạo
4. Chọn **Delete**
   ![01-clean](/images/11/11-clean-01.png?width=90pc)
5. Trong giao diện **Delete bucket**

   - Chọn **Empty bucket**
     ![02-clean](/images/11/11-clean-02.png?width=90pc)

6. Trong giao diện **Empty bucket**

   - Nhập `permanently delete` vào mục **confirm**
   - Chọn **Empty**
     ![03-clean](/images/11/11-clean-03.png?width=90pc)

7. Sau khi **Empty** thành công

   - Chọn **Bucket**
   - Chọn lại **Bucket name** mà bạn muốn xóa
   - Chọn **Delete**
     ![01-clean](/images/11/11-clean-01.png?width=90pc)

8. Trong giao diện **Delete bucket**
   - Copy **Bucket name** mà bạn đã tạo
   - Dán vào mục **confirm**
   - Chọn **Delete bucket**
     ![04-clean](/images/11/11-clean-04.png?width=90pc)

#### Xóa Cloudfront

1. Truy cập vào giao diện của **Cloudfront**
2. Chọn **Distributions**
3. Chọn **Distribution ID** bạn đã tạo
4. Chọn **Disable**
   ![05-clean](/images/11/11-clean-05.png?width=90pc)
   ![06-clean](/images/11/11-clean-06.png?width=90pc)
5. Đợi khoảng vài phút, sau đó chọn **Delete**

#### Xóa Route 53

1. Truy cập vào giao diện của **Route 53**
2. Chọn **Hosted zones**
3. Chọn **Hosted zone name** bạn đã tạo
4. Chọn **Delete**
   ![07-clean](/images/11/11-clean-07.png?width=90pc)
5. Trong giao diện **Delete hosted zone**
   - Nhập `delete` vào mục **confirm**
   - Chọn **Delete**
     ![08-clean](/images/11/11-clean-08.png?width=90pc)

#### Xóa SNS

1. Truy cập vào giao diện của **SNS**
2. Chọn **Topics**
3. Chọn **Topic name** bạn đã tạo
4. Chọn **Delete**
   ![09-clean](/images/11/11-clean-09.png?width=90pc)
5. Trong giao diện **Delete topic**
   - Nhập `delete me` vào mục **confirm**
   - Chọn **Delete**
     ![10-clean](/images/11/11-clean-10.png?width=90pc)

#### Xóa Cognito

1. Truy cập vào giao diện của **Cognito**
2. Chọn **User pools**
3. Chọn **User pool name** bạn đã tạo
4. Chọn **Delete**
   ![11-clean](/images/11/11-clean-11.png?width=90pc)
5. Trong giao diện **Delete user pool**
   - Chọn **Delete Cognito domain _fcj06f03_ that you assigned** và **Deactivate deletion protection**
   - Nhập tên **user pool** của bạn vào mục **confirm**
   - Chọn **Delete**
     ![12-clean](/images/11/11-clean-12.png?width=90pc)

#### Xóa DynamoDB

1. Truy cập vào giao diện của **DynamoDB**
2. Chọn **Tables**
3. Chọn **Table name** bạn đã tạo
4. Chọn **Delete**
   ![13-clean](/images/11/11-clean-13.png?width=90pc)
5. Trong giao diện **Delete table**
   - Chọn **Delete all CloudWatch alarms for FCJ-DynamoDB.**
   - Nhập `confirm` vào mục **confirm**
   - Chọn **Delete**
     ![14-clean](/images/11/11-clean-14.png?width=90pc)

#### Xóa Lambda

1. Truy cập vào giao diện của **Lambda**
2. Chọn **Functions**
3. Chọn **Function name** bạn đã tạo
4. Chọn **Actions**
5. Chọn **Delete**
   ![15-clean](/images/11/11-clean-15.png?width=90pc)
6. Trong giao diện **Delete functions**
   - Nhập `delete` vào mục **confirm**
   - Chọn **Delete**
     ![16-clean](/images/11/11-clean-16.png?width=90pc)

#### Xóa API Gateway

1. Truy cập vào giao diện của **API Gateway**
2. Chọn **APIs**
3. Chọn **API name** bạn đã tạo
4. Chọn **Delete**
   ![17-clean](/images/11/11-clean-17.png?width=90pc)
5. Trong giao diện **Delete API**
   - Nhập `confirm` vào mục **confirm**
   - Chọn **Delete**
     ![18-clean](/images/11/11-clean-18.png?width=90pc)

#### Xóa WAF

1. Truy cập vào giao diện của **WAF**
2. Chọn **Web ACLs**
3. Chọn **Web ACL name** bạn đã tạo
4. Chọn **Associated AWS resources**
5. Chọn **Disassociate**
   ![21-clean](/images/11/11-clean-21.png?width=90pc)
6. Trong giao diện **Disassociate**
   - Nhập `remove` vào mục **confirm Disassociation**
   - Chọn **Disassociate**
     ![22-clean](/images/11/11-clean-22.png?width=90pc)
7. Vào lại **Web ACLs**
8. Chọn **Web ACL name** bạn đã tạo
9. Chọn **Delete**
   ![19-clean](/images/11/11-clean-19.png?width=90pc)
10. Trong giao diện **Delete**
    - Nhập `delete` vào mục **confirm**
    - Chọn **Delete**
      ![20-clean](/images/11/11-clean-20.png?width=90pc)
