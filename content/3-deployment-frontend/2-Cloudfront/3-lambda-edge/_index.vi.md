+++
title = "Cấu hình Lambda@Edge cho Origin Website"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>2.2.3 </b>"
+++

#### Cấu hình Lambda@Edge cho Origin Website

1. Ở giao diện **Cloudfront**

   - Chọn **Functions**
   - Chọn **Create function**
     ![16-Cloudfront](/images/4/4-cloudfront-16.png?width=90pc)

2. Ở giao diện **Create function**

   - Nhập **Name**: `fcj-lambda-edge`
   - Ở phần **Runtime** chọn **cloudfront-js-2.0**
   - Chọn **Create function**
     ![17-Cloudfront](/images/4/4-cloudfront-17.png?width=90pc)

3. Ở giao diện **Functions**

   - Chọn **Functions** mà bạn vừa tao
     ![18-Cloudfront](/images/4/4-cloudfront-18.png?width=90pc)

   - Kéo xuống mục **Build**
   - Ở phần **Function code** chọn **Development**
   - Copy dòng code này vào:

   ```
   function handler(event) {
   var request = event.request;
   var uri = request.uri;

   // Check whether the URI is missing a file name.
   if (uri.endsWith('/')) {
       request.uri += 'index.html';
   }
   // Check whether the URI is missing a file extension.
   else if (!uri.includes('.')) {
       request.uri += '/index.html';
   }

   return request;
   }
   ```

   - Sau đó chọn **Save changes**
     ![19-Cloudfront](/images/4/4-cloudfront-19.png?width=90pc)

   - Chuyển qua mục **Publish**
   - Chọn **Publish function**
     ![20-Cloudfront](/images/4/4-cloudfront-20.png?width=90pc)

4. Quay lại giao diện **Distributions**

   - Chọn **Distributions** bạn đã tạo
   - Chọn **Behaviors**
   - Chọn **Behavior** có origin forward sang **S3** của bạn
   - Sau đó chọn **Edit**
     ![21-Cloudfront](/images/4/4-cloudfront-21.png?width=90pc)

5. Ở giao diện **Edit**

   - Kéo xuống tìm **Function associations - optional**
   - Cấu hình với **Viewer request**
   - **Function type** chọn **CloudFront Functions**
   - **Function ARN / Name** chọn **fcj-lambda-edge** bạn vừa tạo ở trên
   - Chọn **Save changes**
     ![22-Cloudfront](/images/4/4-cloudfront-22.png?width=90pc)
