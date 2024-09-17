+++
title = "Configure Route 53 and Certificate Manager"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3.3 </b>"
+++

#### Configure Route 53

1. Access the
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find **Route 53**
   - Select **Route 53**
     ![01-Route53-ACM](/images/3/3-route53-acm-01.png?width=90pc)

2. Trong giao diện **Route 53**

   - Find **Hosted zones**
   - Select **Create hosted zone**
     ![02-Route53-ACM](/images/3/3-route53-acm-02.png?width=90pc)

3. In the **Create hosted zone** interface

   - Write the **Domain name** registered in the previous post
   - In the Type section, select Public hosted zone
   - Select **Create hosted zone**
     ![03-Route53-ACM](/images/3/3-route53-acm-03.png?width=90pc)

4. Return to the **Hosted zones** interface

   - Go to the Hosted zone name you just created
     ![04-Route53-ACM](/images/3/3-route53-acm-04.png?width=90pc)

   - Select **Create record**

![05-Route53-ACM](/images/3/3-route53-acm-05.png?width=90pc)

5. In the **Create record** interface

   - **Record type** select **CNAME**
   - **Record name** enter 'workshop'
   - **Value** enter **Distribution domain name** of **Cloudfront** (e.g. 'https://d23akwur3rh4c.cloudfront.net') - Select **Create records**
     ![06-Route53-ACM](/images/3/3-route53-acm-06.png?width=90pc)

#### Configuring the Certificate Manager

1. Access the
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find `Certificate Manager`
   - Select **Certificate Manager**
     ![08-Route53-ACM](/images/3/3-route53-acm-08.png?width=90pc)

2. In the **Certificate Manager** interface

   - Moved **Region** to **N.Virginia**
     ![07-Route53-ACM](/images/3/3-route53-acm-07.png?width=90pc)

   - Select **Request certificate**
   - **Certificate type** select **Request a public certificate**
   - Select **Next**
     ![09-Route53-ACM](/images/3/3-route53-acm-09.png?width=90pc)

   - In the **Request public certificate** section
   - **Domain names** enter **workshop.conglyblog.id.vn**
     ![10-Route53-ACM](/images/3/3-route53-acm-10.png?width=90pc)

   - The rest keeps the default - Scroll down and select **Request**
     ![11-Route53-ACM](/images/3/3-route53-acm-11.png?width=90pc)

3. After the **Request** is successful

   - Find **Domains**
   - Select **Create records in Route 53**
     ![12-Route53-ACM](/images/3/3-route53-acm-12.png?width=90pc)

   - **records** have now been created
     ![14-Route53-ACM](/images/3/3-route53-acm-14.png?width=90pc)

   - Go to **Route 53** and check again
     ![13-Route53-ACM](/images/3/3-route53-acm-13.png?width=90pc)

   - Congratulations, you have successfully created a **Certificate** for your domain name.
