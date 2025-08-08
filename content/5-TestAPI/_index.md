---
title : "Test API on PostMan"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

#### TEST UPLOADING BASE64 IMAGE API ON POSTMAN 
In this project, we use Base64. The purpose of Base64 in uploading images to S3 via Lambda and API Gateway is to transmit image data over the network (HTTP) safely and easily in text-only environments such as JSON or Lambda.

1. What is Base64?
- Base64 is a way to encode binary data into text (character strings), making it possible to send files (images, audio, etc.) through systems that only support text, such as:
  + JSON
  + HTML
  + HTTP request body
- Advantages of using Base64
  + Easy to embed in JSON ("body": "{ imageBase64: '...'}")
  + No need for complex configuration like multipart/form-data
  + Easy to test in the Lambda console

- In this project, Base64 helps encode images into text strings to send through API Gateway easily, and Lambda can decode them to upload to S3. This is a simple and effective solution for transmitting images in environments that do not support direct file uploads, such as Lambda Console or API Gateway.
2. Test API on PostMan
- As above, we have the URL:
~~~
https://co9tjkrvjc.execute-api.us-east-1.amazonaws.com/prod/uploads
~~~
- Next, let's proceed on PostMan
  + Method : POST
  + URL    : The API you just created
  + Header : "" Content-Type: application/json ""
  + Body   :
    ~~~
    {"image": "/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxISEh..."}
    ~~~
- The image link is converted to base64
![API](/images/32.png)
![API](/images/33.png)
- Then click Send and the result will be displayed below:
![API](/images/34.png)

3. Check the result on S3 
- After Postman notifies that the upload was successful, go to S3 to check if the image has been uploaded
- As shown in the image, it was successful
![API](/images/35.png)
- If you want to view the image in detail, select the image you want to view, when the interface opens, select **Open**
- You will then be redirected to a new page and the image will be displayed
![API](/images/36.png)
![API](/images/37.png)

So you have successfully uploaded an image to S3