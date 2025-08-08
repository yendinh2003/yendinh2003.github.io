---
title : "Create S3 Bucket"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Initialize S3 Bucket for Storing Images and Results

Access the Console and find the Amazon S3 service
  - Go to the [AWS Management Console](https://aws.amazon.com/vi/console/)
  - Log in to your account
  - After successful login, you will be redirected to the main **AWS Management Console** page as shown below:
    ![S3](/images/console.png)
  - Search for S3 in the search bar and select the S3 service
    ![S3](/images/S3-1.png)
  - Click "Create bucket" and follow the instructions

S3 Configuration

  In the **General configuration** section:
  - AWS Region: choose the region you want to use
  - Bucket type: select General purpose
  - Bucket name: enter fjc-s3bucket

  In the **Object Ownership** section:
  - Select **ACLs disable (recommended)**
   ![S3](/images/S3-3.png)

   In the **Block Public Access setting for this bucket** section:
   - Uncheck **Block all public access**
   - Check **I acknowledge that the current settings might result in this bucket and the objects within becoming public.**
      ![S3](/images/S3-4.png)

  Keep the default settings for the remaining options, then select Create Bucket
  - Wait a few seconds and you will be redirected to the bucket list page with a success message as shown below:
      ![S3](/images/S3-5.png)