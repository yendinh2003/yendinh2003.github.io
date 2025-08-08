---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Amazon S3 (Simple Storage Service)** is AWS's object storage service that allows users to store and retrieve any type of data, such as images, videos, documents, or large data files. Data in S3 is stored in "buckets" and can be accessed via a URL or API. S3 offers virtually unlimited storage capacity, high durability, and strong integration with other services in the AWS ecosystem. It is an ideal choice for storing static files, data backups, or distributing content over the internet.

**Amazon API Gateway** is a service that enables the creation, publishing, management, and securing of APIs at scale. It serves as the communication gateway between clients (e.g., browsers, mobile apps) and backend services such as AWS Lambda or EC2 servers. With API Gateway, you can easily build RESTful or HTTP APIs to receive and process user requests. This service supports version management, rate limiting, authentication, and logging, making the API deployment process fast, secure, and easy to control.

**AWS Lambda** is AWS’s serverless computing service that allows you to run code without having to manage physical or virtual servers. Lambda works on an event-driven model—meaning that when an event occurs (e.g., a file is uploaded to S3 or a request comes from API Gateway), Lambda automatically executes the code you’ve written. You only need to focus on the processing logic, while AWS handles the deployment, scaling, and operations. Lambda supports multiple languages such as Python, Node.js, Java, and Go, making it well-suited for small applications, automation tasks, and flexible backend systems.

By using Amazon S3, you gain the following advantages:
You can store millions or even billions of files without worrying about storage limitations.
~~
Data durability is guaranteed up to 99.999999999% (11 nines), ensuring safety for long-term storage.

Each file has its own unique URL and can be accessed directly via the web or through an API.

You can control access to each file or bucket using policies, IAM, or ACLs.

Works seamlessly with services like Lambda, CloudFront, API Gateway, Athena, etc.

Amazon S3 is a powerful, flexible, and reliable cloud storage solution suitable for both individuals and businesses of all sizes. With unlimited storage capacity, extremely high data durability, and deep integration with the AWS ecosystem, S3 is a top choice for storing images, videos, documents, backups, and static content for websites or applications. Thanks to its flexible access control and permissions model, Amazon S3 not only ensures safe storage but also supports the deployment of modern systems like serverless architectures with ease and efficiency.