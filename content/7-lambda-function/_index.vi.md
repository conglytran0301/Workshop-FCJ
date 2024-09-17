+++
title = "Triển khai Lambda function"
date = 2020-05-14T00:38:32+07:00
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

#### Triển khai Lambda function

1. Truy cập vào
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Tìm **Lambda**
   - Chọn **Lambda**
     ![01-Lambda](/images/8/8-lambda-01.png?width=90pc)

2. Trong giao diện **Lambda**

   - Chọn **Create a function**
     ![02-Lambda](/images/8/8-lambda-02.png?width=90pc)

3. Trong giao diện **Create function**

   - Chọn **Author from scratch**
   - **Function name** nhập `FCJ-LambdaFunction`
   - **Runtime** chọn **Python 3.9**
   - **Architecture** chọn **x86_64**
   - Kéo xuống và chọn **Create function**
     ![03-Lambda](/images/8/8-lambda-03.png?width=90pc)

   - Sau khi tạo bạn sẽ thấy giao diện sau đây
     ![04-Lambda](/images/8/8-lambda-04.png?width=90pc)

4. Nhập **Source code** cho **Lambda Function**

   - Chọn **Code**
   - Dán **code** vào
     ![05-Lambda](/images/8/8-lambda-05.png?width=90pc)

   ```import json  # Đảm bảo đã import json
   import boto3
   import uuid

   # Tạo tài nguyên DynamoDB
   dynamodb = boto3.resource('dynamodb')

   # Đặt tên bảng DynamoDB
   table = dynamodb.Table('FCJ-DynamoDB')

   # Tạo một SNS Client
   client_sns = boto3.client('sns')

   # Hàm này sẽ được kích hoạt bởi API Gateway
   def lambda_handler(event, context):
       try:
           # Kiểm tra sự tồn tại của các key bắt buộc
           required_keys = ['name', 'email', 'subject', 'description']
           for key in required_keys:
               if key not in event:
                   raise KeyError(f"Missing required key: {key}")

           # Tạo một ID người dùng
           id = str(uuid.uuid4())

           # Gửi tin nhắn đến SNS
           handle_sns(id, event)

           # Lưu trữ dữ liệu vào DynamoDB
           statusCode = handle_dynamo_db(id, event)

           return {
               'statusCode': statusCode,
           }

       except KeyError as ke:
           return {
               'statusCode': 400,
               'body': json.dumps(f"Missing required key: {str(ke)}")
           }

       except Exception as e:
           return {
               'statusCode': 500,
               'body': json.dumps('Error occurred: ' + str(e))
           }

   # Gửi một tin nhắn đến SNS
   def handle_sns(id, event):
       try:
           sns_message = f"""
               You got a new Message from https://workshop.conglyblog.id.vn
               The message is as follows

               id      : {id}
               Name    : {event['name']}
               email   : {event['email']}
               Message : {event['description']}
               Subject : {event['subject']}
           """

           client_sns.publish(
               # Thay đổi ARN với ARN của SNS của bạn
               TopicArn='arn:aws:sns:ap-southeast-1:336760284039:FCJ-SNSTopic',
               Message=sns_message,
               Subject=event['subject']
           )

       except KeyError as ke:
           print(f"Key error: {ke}")
           raise

       except Exception as e:
           print(f"An error occurred when sending SNS: {e}")
           raise

   # Thêm một mục vào bảng DynamoDB
   def handle_dynamo_db(id, event):
       try:
           response = table.put_item(
               Item={
                   'id': id,
                   'name': event['name'],
                   'email': event['email'],
                   'subject': event['subject'],
                   'description': event['description'],
               }
           )
           return response['ResponseMetadata']['HTTPStatusCode']

       except Exception as e:
           print(f"An error occurred when writing to DynamoDB: {e}")
           raise
   ```

   {{% notice note %}}
   Thay đổi tên miền này của đoạn code trên: **"You got a new Message from https://workshop.conglyblog.id.vn"** thành **tên miền** của bạn.
   {{% /notice %}}

   - Chọn **Deploy**
     ![06-Lambda](/images/8/8-lambda-06.png?width=90pc)

5. Cấu hình **IAM Roles** cho Lambda

   - Chọn **Configuration**
   - Chọn **Permissions**
   - Chuyển hướng đến **IAM Roles**
     ![07-Lambda](/images/8/8-lambda-07.png?width=90pc)

6. Trong giao diện **Permissions**

   - Chọn **Add permissions**
   - Chọn **Attach policies**
     ![11-Lambda](/images/8/8-lambda-11.png?width=90pc)

   - Tìm **SNS**
   - Chọn **AmazonSNSFullAccess**
     ![09-Lambda](/images/8/8-lambda-09.png?width=90pc)

   - Tiếp tục, tìm **DynamoDB**
   - Chọn **AmazonDynamoDBFullAccess**
   - Chọn **Add permissions**
     ![10-Lambda](/images/8/8-lambda-10.png?width=90pc)

#### Tài liệu tham khảo

- [Building Lambda functions with Python](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html)
