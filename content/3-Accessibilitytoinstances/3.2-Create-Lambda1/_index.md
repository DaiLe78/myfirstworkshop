---
title : "Create Lambda1"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---


#### Create Lambda1 function 
1. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Click **Creat Function**.
  + Choose **Author from scratch**.
  + In the **Function name** section enter **Lambda1**.
  + Choose language **Python 3.13**.
  + The rest remains default. Then click on **Create function**.

![Lambda1](/images/3.connect/Lambda1-01.png)

{{%notice tip%}}
We will update the code for Lambda1 later after creat DynamoDB in the next step. The purpose is to be able to connect Lambda1 to DynamoDB.
{{%/notice%}}

### Connect Lambda1 to Lex to handle backend logic
2. Go to [LEX service management console](https://ap-southeast-2.console.aws.amazon.com/lexv2/home)
  + Click on **Aliases** in the left menu.
  + In the **Languages** section, click on **English (US)**.    
![Lambda1](/images/3.connect/Lambda1-02.png)
  + In the **Source** section choose **Lambda1** and the version is **$LATEST**. This step will add **Lambda1** function into **LEX**.
![Lambda1](/images/3.connect/Lambda1-03.png)
  + Go to **Intents** in the left menu, tick on **Use a Lambda function for fullfilment** in order to display fullfliment in the lambda's code.
![Lambda1](/images/3.connect/Lambda1-04.png)

Okay we have created Lambda1 function and connect it to LEX. Now we will move to the next step!


