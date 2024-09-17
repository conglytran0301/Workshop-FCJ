+++
title = "Create Cloudfront"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>2.2.1 </b>"
+++

#### Create Cloudfront

1. Access the
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find **Cloudfront**
   - Select **Cloudfront**
     ![01-Cloudfront](/images/4/4-cloudfront-01.png?width=90pc)

2. In the **Cloudfront** interface

   - Select **Distributions**
   - Select **Create distribution**
     ![02-Cloudfront](/images/4/4-cloudfront-02.png?width=90pc)

3. In the **Create distribution** interface

   - **Origin domain**, select the name of the created **S3 bucket**
   - **Origin access**, select **Origin access control settings (recommended)**
   - **Origin access control**, select **Create new OAC**
     ![03-Cloudfront](/images/4/4-cloudfront-03.png?width=90pc)

   - In the Create new OAC interface, leave it to default. Then select **Create**
     ![04-Cloudfront](/images/4/4-cloudfront-04.png?width=90pc)

   - After **Create new OAC**, select the OAC you just created
     ![15-Cloudfront](/images/4/4-cloudfront-15.png?width=90pc)

   - Scroll down to the **Viewer protocol policy** section, select **Redirect HTTP to HTTPS**

   - In the Allowed HTTP methods section, select **GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE**
     ![06-Cloudfront](/images/4/4-cloudfront-06.png?width=90pc)

   - In the Web Application Firewall (WAF) section, select **Do not enable security protections**
     ![07-Cloudfront](/images/4/4-cloudfront-07.png?width=90pc)

   - The rest is left to default. Scroll down and select **Create distribution**
     ![08-Cloudfront](/images/4/4-cloudfront-08.png?width=90pc)

   - Congratulations on successfully creating **Distribution**
   - The initialization process will take 4-5 minutes to complete.
