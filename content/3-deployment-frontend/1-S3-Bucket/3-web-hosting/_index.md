+++
title = "Enable Static website hosting"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3.1.3 </b>"
+++

#### Enable Static website hosting

1. Go to the created S3 bucke

   - Select **Properties**
     ![13-S3](/images/3/3-s3-13.png?width=90pc)

2. In the **Properties** interface

   - Scroll down to find **_Static website hosting_** and select **Edit**
     ![14-S3](/images/3/3-s3-14.png?width=90pc)

3. In the interface **Edit static website hosting**

   - In the Static website hosting section, select Enable
   - In the **Hosting type** section, select **Host a static website**
   - In the Index document section, enter `index.html`
   - In the Error document section, enter `error.html`
     ![15-S3](/images/3/3-s3-15.png?width=90pc)

   - Scroll down and select **Save changes**
     ![16-S3](/images/3/3-s3-16.png?width=90pc)
