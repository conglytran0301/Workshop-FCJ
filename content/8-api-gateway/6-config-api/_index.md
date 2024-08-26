+++
title = "API Configuration"
date = 2020-05-14T00:38:32+07:00
weight = 6
chapter = false
pre = "<b>8.6 </b>"
+++

#### API Configuration

1. In the **API** interface

- Select **Stages**
- Select **Dev**
- Copy **Invoke URL** 'https://7s5pb02ska.execute-api.ap-southeast-1.amazonaws.com/Dev'

![18-API](/images/9/9-api-18.png?width=90pc)

2. In the **code web** interface

- Find the file **api.js**
- Paste the **Invoke URL** into line 8 and add `/serverless` after it.

![20-API](/images/9/9-api-20.png?width=90pc)

- Save and upload to **S3**
