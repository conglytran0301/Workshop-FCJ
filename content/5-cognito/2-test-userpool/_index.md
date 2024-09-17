+++
title = "Check out Cognito User pool"
date = 2024-08-19T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>5.2 </b>"
+++

#### Check out Cognito User pool

1. In the **User pool** interface

   - Select the **User pool** that you just created
     ![14-Cognito](/images/6/6-cognito-14.png?width=90pc)

   - Select **App integration**
     ![15-Cognito](/images/6/6-cognito-15.png?width=90pc)

   - Scroll down to the **App clients and analytics** section
   - Select the **App client name** you created
     ![16-Cognito](/images/6/6-cognito-16.png?width=90pc)

   - Scroll down to the **Hosted UI** section
   - Select **View Hosted UI**
     ![17-Cognito](/images/6/6-cognito-17.png?width=90pc)

   {{% notice note %}}You have opened the account registration page of **Cognito**, but you have not yet entered the 1st interface (/index.html). To access this interface, you need to add the _link URL_ of Cognito to your website code.
   {{% /notice %}}

2. In the Login interface of **Cognito**

   - Select **copy** the link on **Cognito's login page**
     ![26-Cognito](/images/6/6-cognito-26.png?width=90pc)

   - Open the **code** you cloned
   - Select the file **index.html**. Find line "Change - Sign in Link" and paste the link.
     ![30-Cognito](/images/6/6-cognito-30.png?width=90pc)

   - Next, select the file **contact-me.html**. Find line "Change - SignOut URL" and paste the link.
     ![29-Cognito](/images/6/6-cognito-29.png?width=90pc)

   ```
   //The SignIn and SignOut paths have the following structure:

   MAKE URL OF SIGN IN /login?client_id=&response_type=token&scope=aws.cognito.signin.user.admin+email+openid+phone+profile&redirect_uri=

   MAKE URL OF SIGN OUT /logout?client_id=&response_type=token&scope=aws.cognito.signin.user.admin+email+openid+phone+profile&redirect_uri=
   ```

   - Then go to the **main.js** file
   - Find **window.location.href** and paste your domain name with the `/index.html`.
     ![28-Cognito](/images/6/6-cognito-28.png?width=90pc)

   - Then update again on your S3.

3. Go back to the website interface

   - After updating on S3, you return to the **Hosted UI** interface
   - Select **View Hosted UI**
   - At this time, you have entered the 1st website
   - Select **LOGIN**
     ![18-Cognito](/images/6/6-cognito-18.png?width=90pc)

   - Select **Sign up** to register for an account
     ![19-Cognito](/images/6/6-cognito-19.png?width=90pc)

   - **Username** enter '_Your Username_'
   - **Email** enter '_Your Email_'
   - **Password** enter '_Your Password_'
     ![20-Cognito](/images/6/6-cognito-20.png?width=90pc)

   - Go to the **Email** you just registered to get **code**
     ![21-Cognito](/images/6/6-cognito-21.png?width=90pc)

   - **Code** has been sent to your **Email**
     ![22-Cognito](/images/6/6-cognito-22.png?width=90pc)

   - Copy the **code** and paste it into the box of **Verification code**
   - Then select **Confirm account**
     ![23-Cognito](/images/6/6-cognito-23.png?width=90pc)

   - Congratulations, you have successfully registered an account and entered the 2nd interface
     ![25-Cognito](/images/6/6-cognito-25.png?width=90pc)
