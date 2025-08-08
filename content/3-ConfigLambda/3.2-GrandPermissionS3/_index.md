---
title : "Grand Permission S3"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---
#### Grant S3 Permissions to Lambda Function (in IAM Console) ####

1. Method 1: Grant Full S3 Access (easy, quick)
- In the IAM interface, on the left sidebar, select **Role**
- You will see a **Role** with the same name as the function you just created
- Click on that **Role**
- The result should look like the image below:  
![Lambda](/images/17.png)

- After accessing the **Role** interface:
- In the **Permissions policies** section:
- Select **Add permission** and then choose **Attach Policies**
![Lambda](/images/18.png)

You will see the full list of **Permissions Policies**
- In the Search bar, search for **AmazonS3FullAccess**
- Select that policy and click **Add permission**
![lambda](/images/19.png)
📌 Result: Your Lambda now has full access to all S3 buckets

2. Method 2: Grant permission to upload images to only one bucket (safer)
- Go back to the **Role** for your function
- In the **Permissions policies** section:
- Select **Add permission** and then **Create inline policy**
![Lambda](/images/20.png)

- After entering the **Create policy** interface
- In the **Specify permission** section, you can enter the following code to configure permissions, then click Next:
~~~json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:PutObject"
      ],
      "Resource": "arn:aws:s3:::fjc-s3bucket/*"
    }
  ]
}
~~~
![Lambda](/images/21.png)

- Next, on the **Review and create** interface:
- Policy name: LambdaS3UploadOnly
- Then click **Create policy**
- After creation, you will be returned to the **Role** screen and a success notification will appear
![Lmabda](/images/22.png)

📌 After completion, your Lambda can now successfully upload images to the S3 bucket.