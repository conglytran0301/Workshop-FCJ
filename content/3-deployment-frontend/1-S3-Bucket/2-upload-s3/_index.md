+++
title = "Upload Data"
date = 2020-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>3.1.2 </b>"
+++

#### Upload Data

{{% notice note %}}
we'll upload _source code_ to the S3 bucket for storage. If you haven't downloaded the _source code_ yet, go back to [2.1.Clone repository from Github](2-preparation/1-clone-code) to clone the repo.
{{% /notice %}}

1. In the S3 bucket you just created

- There is currently no **Object** in **Bucket**
- Select **Upload** to upload your data

![08-S3](/images/3/3-s3-08.png?width=90pc)

2. In the **Upload** interface

- Go to the **Folder** named _**FCJ-Serverless**_ that was _cloned_ from **Github** in the above step
- Press **CRLT + A** key combination to select all folders
- Then drag the entire Folder and File and drop it into the **Upload** interface of the **S3 bucket**.

![09-S3](/images/3/3-s3-09.png?width=90pc)

- Once all folders have been selected, drop them into **Bucket**

![10-S3](/images/3/3-s3-10.png?width=90pc)

- Scroll down to the bottom of the page and select **Upload**

![11-S3](/images/3/3-s3-11.png?width=90pc)

- Once the Upload is complete, you will see the files that have been added to the S3 Bucket

![12-S3](/images/3/3-s3-12.png?width=90pc)
