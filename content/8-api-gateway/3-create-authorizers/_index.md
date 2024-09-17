+++
title = "Create Authorizer"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>8.3 </b>"
+++

#### Create Authorizer

1. In the **API**

   - Select **Authorizers**
   - Select **Create authorizer**
     ![10-API](/images/9/9-api-10.png?width=90pc)

2. In the **Create authorizer** interface

   - **Authorizer name** enter `FCJ-Auth`
   - **Authorizer type** select **Cognito**
   - **Cognito user pool** select **FCJ-UserPool**
   - **Token source** enter `Authorization`
   - Select **Create authorizer**
     ![11-API](/images/9/9-api-11.png?width=90pc)

3. Go to the **Resources** interface

   - Select **GET**
   - Select **Method request**
   - Select **Edit**
     ![12-API](/images/9/9-api-12.png?width=90pc) 4. In the **Edit method request** interface

   - **Authorization** select **FCJ-Auth**
   - **Authorization scopes** enter `email`, then select **add**
   - Scroll down and select **Save**
     ![13-API](/images/9/9-api-13.png?width=90pc)
