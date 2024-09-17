+++
title = "Initialize Cognito User pool"
date = 2024-08-19T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++

#### Initialize Cognito User pool

1. Access the
   [AWS Management Console](https://aws.amazon.com/vi/free/?gclid=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE&trk=c4f45c53-585c-4b31-8fbf-d39fbcdc603a&sc_channel=ps&ef_id=CjwKCAjw_ZC2BhAQEiwAXSgClvWbbk-Y8aK5QEAweAN7K8tLmdmvIiZuLvrcXaHfX9HrfLJlZr3U2xoC6y4QAvD_BwE:G:s&s_kwcid=AL!4422!3!637354294239!e!!g!!aws!19043613274!143453611386&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

   - Find **Cognito**
   - Select **Cognito**
     ![01-Cognito](/images/6/6-cognito-01.png?width=90pc)

2. In the **Cognito** interface

   - Select **Create user pool**
     ![02-Cognito](/images/6/6-cognito-02.png?width=90pc)

3. In the **Create user pool** interface

   In Step 1 **Configure sign-in experience**

   - Find **Cognito user pool sign-in options**, select **User name** and **Email**
   - Select **Next**
     ![03-Cognito](/images/6/6-cognito-03.png?width=90pc)

   In Step 2 **Configure security requirements**

   - **Password policy mode** select **Cognito defaults**
     ![04-Cognito](/images/6/6-cognito-04.png?width=90pc)

   - **Multi-factor authentication** select **No MFA**
   - **Self-service account recovery** select **Enable self-service account recovery - Recommended**
   - **Delivery method for user account recovery messages** select **Email only**
   - Select **Next**
     ![05-Cognito](/images/6/6-cognito-05.png?width=90pc)

   In Step 3 **Configure sign-up experience**

   - All to **default** - Select **Next**
     ![07-Cognito](/images/6/6-cognito-07.png?width=90pc)

   In Step 4 **Configure message delivery**

   - **Email** select **Send email with Cognito**
   - **FROM email address** select **no-reply@verificationemail.com**
   - Select **Next**
     ![06-Cognito](/images/6/6-cognito-06.png?width=90pc)

   In Step 5 **Integrate your app**

   - **User pool name** enter `FCJUserPool`
   - Select **Use the Cognito Hosted UI**
   - **Domain type** select **Use a Cognito domain**
   - **Cognito domain** enter **Cognito login domain name that you want**
     ![08-Cognito](/images/6/6-cognito-08.png?width=90pc)

   - **App type** select **Public client**
   - **App client name** enter `FCJ-Client`
   - **Allowed callback URLs** enter **http://'domain name assigned to your website'/contact-me.html**

   {{% notice note %}}The 1st web interface is **/index.html** and the 2nd web interface is **/contact-me.html**. When filling in **Allowed callback URLs** there must be **/contact-me.html** after your domain name, so that from the interface of **/index.html** can **callback** to **/contact-me.html**.
   {{% /notice %}}
   ![12-Cognito](/images/6/6-cognito-12.png?width=90pc)

   - Scroll down to find **Advanced app client settings**
   - **OAuth 2.0 grant types**, uncheck **Authorization code grant** and select **Implicit grant**
   - **OpenID Connect scopes** select **OpenID**, **Phone**, **Email**, **aws.cognito.signin.user.admin**, **Profile**
   - **Allowed sign-out URLs - optional** enter **http://'domain name assigned to your site'/index.html**
     ![13-Cognito](/images/6/6-cognito-13.png?width=90pc)

   - Scroll down and select **Next** In Step 6 **Review and create**
   - Check again and select **Create user pool**
     ![10-Cognito](/images/6/6-cognito-10.png?width=90pc)
