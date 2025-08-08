---
title : "Session Management"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Uploading Images to Amazon S3 Using Amazon Lambda and API Gateway

### Overview

- Uploading Images to Amazon S3 Using AWS Lambda and API Gateway is a popular solution for modern web applications to process images serverless.

In this model:
- The user sends an image (Base64 or file format) via API Gateway using the POST method.
- API Gateway passes the data to AWS Lambda.
- Lambda processes image data and uploads it directly to Amazon S3 – a powerful object storage service
### Contents

1. [Introduction](1-introduce/)
2. [Preparation steps](2-Prerequiste/)
3. [Lambda Configuration](3-ConfigLambda/)
4. [API Gateway Configuration](4-ApitoLambda/)
5. [Test API on Postman](5-TestAPI/)
6. [Cleanup resources](6-cleanup/)