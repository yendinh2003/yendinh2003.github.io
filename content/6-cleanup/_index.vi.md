+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa S3 bucket

1. Truy cập [giao diện quản trị S3](https://s3.console.aws.amazon.com/s3/home).

  Chúng ta sẽ thấy giao diện S3 Bucket và tên của bucket vừa tạo 
![S#](/images/38.png)
2. Truy cập [giao diện quản trị dịch vụ S3](https://s3.console.aws.amazon.com/s3/home)
  + Click chọn S3 bucket chúng ta đã tạo cho bài thực hành. ( Ví dụ : fjc-s3bucket )
  + Click **Empty**.
  + Điền **permanently delete**, sau đó click **Empty** để tiến hành xóa object trong bucket.
  + Click **Exit**.

3. Sau khi xóa hết object trong bucket, click **Delete**

![S3](/images/39.png)

4. Điền tên S3 bucket, sau đó click **Delete bucket** để tiến hành xóa S3 bucket.

![S3](/images/40.png)

#### Xóa Lambda Function

Truy cập vào [giao diện quản trị dịch vụ Labmda](https://console.aws.amazon.com/lambda/home#)
  + Click **Function**.
  + Chọn function chúng ta tạo ở trên, Ví dụ : fjc-upload-image
  + Click **Action**.
  + Chọn **Delete**
  + Sau đó nhập **confirm**
  ![lambda](/images/41.png)

#### Xóa Rest API

Truy cập vào [giao diện quản trị dịch vụ API Gateway](https://console.aws.amazon.com/apigateway/home#)
+ Click vào **Api** ở thanh bên
+ Sau đó click vào APIs chúng ta đã tạo ở trên 
+ Click **Delete** và nhập "confirm"
![API](/images/42.png)

Vậy là chúng ta đã hoàn thành việc dọn dẹp tài nguyên