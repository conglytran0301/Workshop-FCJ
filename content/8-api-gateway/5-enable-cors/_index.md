+++
title = "CORS Configuration Setup"
date = 2020-05-14T00:38:32+07:00
weight = 5
chapter = false
pre = "<b>8.5 </b>"
+++

#### CORS Configuration Setup

1. In the **API** interface

   - Select **Resources**
   - Select **/serverless**
   - Select **Enable CORS**
     ![16-API](/images/9/9-api-16.png?width=90pc)

2. In the **Enable CORS** interface

   - **Gateway responses** select **Default 4XX** and **Default 5XX**
   - Access-Control-Allow-Methods select **GET**
   - **Access-Control-Allow-Headers** enter `Authorization` at the end of the line
   - Select **Save**
     ![17-API](/images/9/9-api-17.png?width=90pc)
