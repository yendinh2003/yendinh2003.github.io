+++
title = "Clean up resources"
date = 2022
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

We will follow these steps to delete the resources we created in this tutorial.

#### Delete S3 bucket

1. Go to the [S3 management console](https://s3.console.aws.amazon.com/s3/home).

  You will see the S3 Bucket interface and the name of the bucket you just created.
![S#](/images/38.png)
2. Go to the [S3 service management console](https://s3.console.aws.amazon.com/s3/home)
  + Click on the S3 bucket you created for this tutorial. (For example: fjc-s3bucket)
  + Click **Empty**.
  + Enter **permanently delete**, then click **Empty** to delete the objects in the bucket.
  + Click **Exit**.

3. After deleting all objects in the bucket, click **Delete**.

![S3](/images/39.png)

4. Enter the name of the S3 bucket, then click **Delete bucket** to delete the S3 bucket.

![S3](/images/40.png)

#### Delete Lambda Function

Go to the [Lambda service management console](https://console.aws.amazon.com/lambda/home#)
  + Click **Function**.
  + Select the function you created above, for example: fjc-upload-image
  + Click **Action**.
  + Select **Delete**
  + Then enter **confirm**
  ![lambda](/images/41.png)

#### Delete Rest API

Go to the [API Gateway management console](https://console.aws.amazon.com/apigateway/home#)
+ Click on **Api** in the sidebar
+ Then click on the APIs you created above
+ Click **Delete** and enter "confirm"
![API](/images/42.png)

So we have completed cleaning up the resources.