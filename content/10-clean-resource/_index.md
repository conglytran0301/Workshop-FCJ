+++
title = "Clean up resources"
date = 2024-08-19T00:38:32+07:00
weight = 10
chapter = false
pre = "<b>10. </b>"
+++

We will proceed with the following steps to delete the resources we created in this exercise.

#### Delete S3

1. Access the interface of **S3**
2. Select **Buckets**
3. Select the **Bucket name** you created
4. Select **Delete**
   ![01-clean](/images/11/11-clean-01.png?width=90pc)
5. In the **Delete bucket** interface
   - Select **Empty bucket**
     ![02-clean](/images/11/11-clean-02.png?width=90pc)
6. In the **Empty bucket** interface
   - Type `permanently delete` in **confirm**
   - Select **Empty**
     ![03-clean](/images/11/11-clean-03.png?width=90pc)
7. After **Empty** is successful
   - Select **Bucket**
   - Re-select the Bucket name that you want to delete
   - Select **Delete**
     ![01-clean](/images/11/11-clean-01.png?width=90pc)
8. In the **Delete bucket** interface

   - Copy the **Bucket name** that you created
   - Paste in **confirm**
   - Select **Delete bucket**
     ![04-clean](/images/11/11-clean-04.png?width=90pc)

#### Remove Cloudfront

1. Access the interface of **Cloudfront**
2. Select **Distributions**
3. Select the **Distribution ID** you created
4. Select **Disable**
   ![05-clean](/images/11/11-clean-05.png?width=90pc)
   ![06-clean](/images/11/11-clean-06.png?width=90pc)
5. Wait for a few minutes, then select **Delete**

#### Delete Route 53

1. Access the interface of **Route 53**
2. Select **Hosted zones**
3. Select the **Hosted zone name** you created
4. Select **Delete**
   ![07-clean](/images/11/11-clean-07.png?width=90pc)
5. In the **Delete hosted zone** interface

   - Type `delete` in **confirm**
   - Select **Delete**
     ![08-clean](/images/11/11-clean-08.png?width=90pc)

#### Delete SNS

1. Access the interface of **SNS**
2. Select **Topics**
3. Select the **Topic name** you created
4. Select **Delete**
   ![09-clean](/images/11/11-clean-09.png?width=90pc)
5. In the **Delete topic** interface

- Type 'delete me' in **confirm**
- Select **Delete**
  ![10-clean](/images/11/11-clean-10.png?width=90pc)

#### Remove Cognito

1. Access the interface of **Cognito**
2. Select **User pools**
3. Select the **User pool name** you have created
4. Select **Delete**
   ![11-clean](/images/11/11-clean-11.png?width=90pc)
5. In the **Delete user pool** interface

- Select **Delete Cognito domain _fcj06f03_ that you assigned** and **Deactivate deletion protection**
- Enter the name of your **user pool** in **confirm** field
- Select **Delete**
  ![12-clean](/images/11/11-clean-12.png?width=90pc)

#### Deleting DynamoDB

1.  Access the interface of **DynamoDB**
2.  Select **Tables**
3.  Select the **Table name** you created
4.  Select **Delete**
    ![13-clean](/images/11/11-clean-13.png?width=90pc)
5.  In the **Delete table** interface

- Select **Delete all CloudWatch alarms for FCJ-DynamoDB.**
- Type `confirm` in **confirm**
- Select **Delete**
  ![14-clean](/images/11/11-clean-14.png?width=90pc)

#### Deleting Lambda

1. Access the interface of **Lambda**
2. Select **Functions**
3. Select the **Function name** you created
4. Select **Actions**
5. Select **Delete**
   ![15-clean](/images/11/11-clean-15.png?width=90pc)
6. In the **Delete functions** interface

- Type `delete` in **confirm**
- Select **Delete**
  ![16-clean](/images/11/11-clean-16.png?width=90pc)

#### Deleting API Gateway

1. Access the interface of **API Gateway**
2. Select **APIs**
3. Select the **API name** you created
4. Select **Delete**
   ![17-clean](/images/11/11-clean-17.png?width=90pc)
5. In the **Delete API** interface

- Type `confirm` in **confirm**
- Select **Delete**
  ![18-clean](/images/11/11-clean-18.png?width=90pc)

#### Delete WAF

1. Access the interface of **WAF**
2. Select **Web ACLs**
3. Select the **Web ACL name** you created
4. Select **Associated AWS resources**
5. Select **Disassociate**
   ![21-clean](/images/11/11-clean-21.png?width=90pc)
6. In the **Disassociate** interface

- Type `remove` in **confirm Disassociation**
- Select **Disassociate**
  ![22-clean](/images/11/11-clean-22.png?width=90pc)

7. Re-enter **Web ACLs**
8. Select the Web ACL name you created
9. Select **Delete**
   ![19-clean](/images/11/11-clean-19.png?width=90pc)
10. In the **Delete** interface

- Type `delete` in **confirm**
- Select **Delete**
  ![20-clean](/images/11/11-clean-20.png?width=90pc)
