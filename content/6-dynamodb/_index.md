+++
title = "Initialize DynamoDB"
date = 2020-05-14T00:38:32+07:00
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

#### Initialize DynamoDB

1. Access the
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find **DynamoDB**
   - Select **DynamoDB**
     ![01-DynamoDB](/images/7/7-dynamodb-01.png?width=90pc)

2. In the Dashboard interface of DynamoDB - Select **Create table**
   ![02-DynamoDB](/images/7/7-dynamodb-02.png?width=90pc)

3. In the **Create table** interface

   - **Table name** enter `FCJ-DynamoDB`
   - **Partition key** enter `id` select **string**
   - **Sort key** enter `name` select **string**
     ![03-DynamoDB](/images/7/7-dynamodb-03.png?width=90pc)

   - **Table settings** to default
   - Scroll down and select **Create table**
     ![04-DynamoDB](/images/7/7-dynamodb-04.png?width=90pc)

#### Reference Links

- [Working with tables and data in DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html)
