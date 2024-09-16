+++
title = "Domain Name Registration"
date = 2020-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2.2 </b>"
+++

#### Register a domain name with Amazon Route 53

1. Access the [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find **Route 53**
   - Select **Route 53**
     ![01-Route53](/images/2/2-03-domain.png?width=90pc)

2. In the **Route 53** interface

   - Select **Registered domains**
     ![02-Route53](/images/2/2-04-domain.png?width=90pc)

3. In the **Registered domains** interface

   - Enter the domain name you want to register

   - Select **Search**

   - Click **Select** the domain name you want to register

   - Select **Proceed to checkout**
     ![02-Route53](/images/2/2-05-domain.png?width=90pc)

4. In the **Pricing** section

   - Choice of subscription and renewal time

   - Select **Next**
     ![03-Route53](/images/2/2-06-domain.png?width=90pc)

5. In the **Contact information** section

   - Fill in contact information

   - Select **Next**
     ![04-Route53](/images/2/2-07-domain.png?width=90pc)

6. In the **Review and submit** section

   - Double-check information
   - Select **Submit**
     ![05-Route53](/images/2/2-08-domain.png?width=90pc)

7. Check the domain name

   - Go to **Registered domains** to check the registered domain name information.
     ![06-Route53](/images/2/2-09-domain.png?width=90pc)

   {{% notice info %}}
   If your domain name registration fails, please contact [**AWS Support**](https://support.console.aws.amazon.com/) for assistance.
   {{% /notice %}}

#### Register a domain name with another domain provider

1. Go to the **Console** of the **domain provider** you purchased

   - Select **Manage Domain Name**

   - Select the **domain name** that you **registered**
     ![10-Route53](/images/2/2-10-domain.png?width=90pc)

   - Select **Name Server**

   - Enter the Name Server provided in Route53's Hosted zones
     ![11-Route53](/images/2/2-11-domain.png?width=90pc)

   {{% notice note %}}
   To be able to create DNS from another domain provider to AWS, you need to create Hosted zones in Route 53. Then enter the Name Server provided by Route 53 into the Name Server import of another domain provider. _steps to register for **Hosted zones** you see the instructions at here_: "[Configure Route 53 and Certificate Manager](3-deployment-frontend/3-Route53-ACM)". **Note: Changes may take up to 24 hours to take effect.**
   {{% /notice %}}
