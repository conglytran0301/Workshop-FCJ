+++
title = "WAF Initialization"
date = 2020-05-14T00:38:32+07:00
weight = 4
chapter = false
pre = "<b>3.4 </b>"
+++

#### WAF Initialization

{{% notice note %}}
When you create a Web ACL, it will cost you $5 for 1 month of use.
{{% /notice %}}

1. Access the [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

- Find **WAF**
- Select **WAF**

![01-WAF](/images/3/3-waf-01.png?width=90pc)

2. In the **WAF** interface

- Select **Create web ACL**

![02-WAF](/images/3/3-waf-02.png?width=90pc)

3. In the **Create web ACL** interface

Step 1 **Describe web ACL and associate it to AWS resources**

- **Resource type** select **Amazon CloudFront distributions**
- **Name** enter `WAF-Demo`

![03-WAF](/images/3/3-waf-03.png?width=90pc)

- **Associated AWS resources** select **Add AWS resources**

![04-WAF](/images/3/3-waf-04.png?width=90pc)

- Select the domain name you registered for **Cloudfront**

- Then select **Add**

![05-WAF](/images/3/3-waf-05.png?width=90pc)

- CloudFront distributions select **Default**
- Select **Next**

![06-WAF](/images/3/3-waf-06.png?width=90pc)

Step 2 **Add rules and rule groups**

- **Rules** select **Add rules**

- Select **Add managed rule groups**

![07-WAF](/images/3/3-waf-07.png?width=90pc)

- Select AWS managed rule groups

![08-WAF](/images/3/3-waf-08.png?width=90pc)

- Find the **Free rule groups** section
- **Amazon IP reputation list** select **Add to web ACL**

![09-WAF](/images/3/3-waf-09.png?width=90pc)

- Scroll down and select **Add rules**

![10-WAF](/images/3/3-waf-10.png?width=90pc)

- **Default action** select **Allow**
- Select **Next**

![11-WAF](/images/3/3-waf-11.png?width=90pc)

Step 3 **Set rule priority**

- Select **Next**

![12-WAF](/images/3/3-waf-12.png?width=90pc)

Step 4 **Configure metrics**

- Select **Next**

![13-WAF](/images/3/3-waf-13.png?width=90pc)

- Double-check and select **Create web ACL**

![14-WAF](/images/3/3-waf-14.png?width=90pc)
