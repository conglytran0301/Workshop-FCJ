+++
title = "Deploy Lambda function"
date = 2020-05-14T00:38:32+07:00
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

#### Deploy Lambda function

1. Access the
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find **Lambda**
   - Select **Lambda**
     ![01-Lambda](/images/8/8-lambda-01.png?width=90pc)

2. In the **Lambda** interface

   - Select **Create a function**
     ![02-Lambda](/images/8/8-lambda-02.png?width=90pc)

3. In the **Create function** interface

   - Select **Author from scratch**
   - **Function name** enter `FCJ-LambdaFunction`
   - **Runtime** select **Python 3.9**
   - **Architecture** select **x86_64**
   - Scroll down and select **Create function**
     ![03-Lambda](/images/8/8-lambda-03.png?width=90pc)

   - Once created, you will see the following interface
     ![04-Lambda](/images/8/8-lambda-04.png?width=90pc)

4. Enter the Source code for the Lambda Function

   - Select **Code**
   - Paste **code** into the
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

   {{% notice note %}}Change this domain name of the code above: "You got a new Message from https://workshop.conglyblog.id.vn" to your **domain name**.
   {{% /notice %}}

   - Select **Deploy**
     ![06-Lambda](/images/8/8-lambda-06.png?width=90pc)

5. Configure IAM Roles for Lambda

   - Select **Configuration**
   - Select **Permissions**
   - Redirect to IAM Roles
     ![07-Lambda](/images/8/8-lambda-07.png?width=90pc)

6. In the **Permissions** interface

   - Select **Add permissions**
   - Select **Attach policies**
     ![11-Lambda](/images/8/8-lambda-11.png?width=90pc)

   - Search for **SNS**
   - Select **AmazonSNSFullAccess**
     ![09-Lambda](/images/8/8-lambda-09.png?width=90pc)

   - Go ahead, looking for **DynamoDB**
   - Select **AmazonDynamoDBFullAccess**
   - Select **Add permissions**
     ![10-Lambda](/images/8/8-lambda-10.png?width=90pc)

#### Reference Links

- [Building Lambda functions with Python](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html)
