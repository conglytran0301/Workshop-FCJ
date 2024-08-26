+++
title = "Cloudfront Origin request policy"
date = 2020-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2.2.2 </b>"
+++

#### Cloudfront Origin request policy

1. In the **Distributions** interface

- Select the **Distributions** you just created

![09-Cloudfront](/images/4/4-cloudfront-09.png?width=90pc)

- Select **Origins** - Select the **Origin name** you just created
- Select **Edit** ![10-Cloudfront](/images/4/4-cloudfront-10.png?width=90pc)

2. On the **Edit origin** interface - Select the **OAC** you just created.

- Select **Copy policy** - Redirect to the S3 bucket you created

![05-Cloudfront](/images/4/4-cloudfront-05.png?width=90pc)

- After entering your Bucket, select Permissions

![12-Cloudfront](/images/4/4-cloudfront-12.png?width=90pc)

- Scroll down to find **Bucket policy**, select **Edit**

![13-Cloudfront](/images/4/4-cloudfront-13.png?width=90pc)

- Paste the code into the S3 Bucket policy - Select **Save changes**

![14-Cloudfront](/images/4/4-cloudfront-14.png?width=90pc)

- You have successfully created an **Origin request policy**
