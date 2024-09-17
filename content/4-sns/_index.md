+++
title = "Initialize SNS"
date = 2024-05-14T00:38:32+07:00
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

#### Initialize SNS

1. Access the
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find **SNS**
   - Select **Simple Notification Servicet**
     ![01-SNS](/images/5/5-sns-01.png?width=90pc)

2. In the interface of **SNS**

   - In the Create topic section, enter the Topic name: `FCJ-SNSTopic`
   - Select **Next step**
     ![02-SNS](/images/5/5-sns-02.png?width=90pc)

3. In the interface of **Create topic**

   - In the Type section, select Standard.
     ![03-SNS](/images/5/5-sns-03.png?width=90pc)

   - The rest keeps the default
   - Scroll down to the bottom of the page and select **Create topic**
     ![04-SNS](/images/5/5-sns-04.png?width=90pc)

   - After creating a topic, select Subscriptions in the left sidebar
   - Select **Create subscription**
     ![05-SNS](/images/5/5-sns-05.png?width=90pc)

4. In the **Create subscription** interface

   - In the Topic ARN section, select the Topic you just created
   - **Protocol** select **Email**
   - **Endpoint** enter your **personal email**
   - Then select **Create subscription**
     ![07-SNS](/images/5/5-sns-07.png?width=90pc)

5. After **Create subscription**

   - Go to the email you entered when you created your subscription

   - Select **Confirm subscription** to confirm the subscription
     ![08-SNS](/images/5/5-sns-08.png?width=90pc)

   - You have completed **Confirm subscription**

   {{% notice note %}}After selecting **Confirm subscription** you just need to exit and you're done. (If you choose **click here to unsubscribe**, you will unsubscribe and will not be able to receive **email** information).
   {{% /notice %}}
   ![09-SNS](/images/5/5-sns-09.png?width=90pc)

   #### Reference Links

   - [How to use Amazon SNS with AWS Lambda Function](https://medium.com/cloudnloud/how-to-use-aws-lambda-function-with-amazon-sns-e8fe38097725)
