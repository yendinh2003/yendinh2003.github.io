---
title : "Create REST API"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Configure API Gateway for Image Analysis Function ####

1. Search for and access the API Gateway service
    - In the search bar, type API Gateway and access the service.
    ![API](/images/10.png)
    - After accessing the service, perform the action Create an API.

2. Configure API Gateway 
    - On the API type page, you will see various types of APIs for different purposes such as: **HTTP API**, **REST API**, **WebSocket API**, etc.
    - In this section, we will use **REST API**.

    In the "choose a API type" section:
    - Select **REST API**
    - Click the **Build** button
    - The result will look like this:
      ![API](/images/11.png)

  When you reach the **Create REST API** interface:
    - API details: select **New API**
    - API name: ImageUploadAPI
    - API endpoint type: Regional
    - Then click the Create API button

    After that, you will be redirected to the newly created API and a success message will be displayed.
    ![API](/images/13.png)