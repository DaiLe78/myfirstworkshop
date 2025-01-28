---
title : "Create API Gateway"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 4.3. </b> "
---


#### Create API Gateway 
1. Go to [API Gateway service management console](https://ap-southeast-2.console.aws.amazon.com/apigateway/main)
  + Choose API Type **Rest API**.
  + In the **API details** choose **New API** and part **API name** enter **MyRestAPI**.
![api](/images/4.s3/api-01.png)
  + Click on **Creat API**.
  + Then click on **Creat Method**.
  + In the **Method type** choose **POST** and **Integration type** choose **Lambda function**.
![api](/images/4.s3/api-02.png)
  + In the **Lambda function** section choose **LambdaConnectAPIgwToLex** function.
![api](/images/4.s3/api-03.jpg)
  + The rest remains default. Click on **Creat Method**.
  + Click on **POST** method we created and click on **Enable CORS**.
![api](/images/4.s3/api-04.jpg)
  + In **Access-Control-Allow-Methods** section tick on **POST**.
![api](/images/4.s3/api-05.jpg)
  + Now click on **Deploy API**.
![api](/images/4.s3/api-06.jpg)


Okay we have created API Gateway and connect it to **LambdaConnectAPIgwToLex** function. Now we have a complete Hotel Booking website integrated with Chatbot build on AWS.



