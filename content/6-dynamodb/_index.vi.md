+++
title = "Khởi tạo DynamoDB"
date = 2020-05-14T00:38:32+07:00
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

#### Khởi tạo DynamoDB

1. Truy cập vào
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Tìm **DynamoDB**
   - Chọn **DynamoDB**
     ![01-DynamoDB](/images/7/7-dynamodb-01.png?width=90pc)

2. Ở giao diện **Dashboard** của **DynamoDB**

   - Chọn **Create table**
     ![02-DynamoDB](/images/7/7-dynamodb-02.png?width=90pc)

3. Ở giao diện **Create table**

   - **Table name** nhập `FCJ-DynamoDB`
   - **Partition key** nhập `id` chọn **string**
   - **Sort key** nhập `name` chọn **string**
     ![03-DynamoDB](/images/7/7-dynamodb-03.png?width=90pc)

   - **Table settings** để mặc định
   - Kéo xuống và chọn **Create table**
     ![04-DynamoDB](/images/7/7-dynamodb-04.png?width=90pc)

#### Tài liệu tham khảo

- [Working with tables and data in DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html)
