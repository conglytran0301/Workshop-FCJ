+++
title = "Create an S3 bucket"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>3.1.1 </b>"
+++

#### Create an S3 bucket

1.  Access the
    [AWS Management Console](https://ap-southeast-1.console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin&region=ap-southeast-1)

    - Find **S3**
    - Select **S3**
      ![01-S3](/images/3/3-s3-01.png?width=90pc)

2.  In the **S3** interface

    - Select **Buckets**
    - Select **Create bucket**
      ![02-S3](/images/3/3-s3-02.png?width=90pc)

3.  In the **Create bucket** interface

    - **Bucket name**, enter `s3-workshop-fcj`
    - In the Object Ownership section, select **ACLs disabled**
      ![03-S3](/images/3/3-s3-03.png?width=90pc)

      {{% notice info %}}Note: Because the bucket name is unique on a global scale, if the names are the same, the message "Bucket with the same name already exists" will appear. Therefore, it is necessary to add a few numbers after it to make your bucket name suitable for the policy.
      {{% /notice %}}

      ![04-S3](/images/3/3-s3-04.png?width=90pc)

    - In the Block Public Access settings for this bucket section, leave the default
      ![05-S3](/images/3/3-s3-05.png?width=90pc)

    - The rest remains the default. Scroll down and select **Create bucket**
      ![06-S3](/images/3/3-s3-06.png?width=90pc)

4.  Finish creating an **S3 bucket** to store _source website_
    ![07-S3](/images/3/3-s3-07.png?width=90pc)
