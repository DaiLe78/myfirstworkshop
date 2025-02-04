---
title : "Create SNS and update code for Lambda2"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 3.6. </b> "
---


#### Create SNS 
1. Go to [SNS service management console](https://ap-southeast-2.console.aws.amazon.com/sns/v3/home)
  + Click **Creat Topic**.
  + In the **Topic name** section enter **MyLabSNS**.
  + Choose type **Standard**.
  + In the **Display name** section enter **ChatbotSMS**.
  + The rest remains default. Then click on **Creat topic**.
![SNS](/images/3.connect/SNS-01.png)

2. Go to **Subscriptions** section in the left menu.
  + Click on **Create subscription**.
  + In the **Topic ARN** choose **MyLabSNS ARN** we created.
  + In the **Protocol** section select **Email**.
  + In the **Endpoint** section enter your email address.
![SNS](/images/3.connect/SNS-02.png)

{{%notice tip%}}
After your subscription is created, you must confirm it.
{{%/notice%}}

  + Go to your email address and confirm the subscription.
![SNS](/images/3.connect/SNS-03.png)
  + Successfully established SNS Subscription.

### Update code for Lambda2
3. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Choose **Lambda2** function.
  + Scroll down to **Code Source** section.
  + Replace the default Lambda code with this code. I will put the source code under the following GitHub link.

[Source code Lambda2](https://github.com/DaiLe78/Source-code-Chatbot-AWS/blob/master/Lambda2.py)
  + After this step, we will have the following architecture diagram
![SNS](/images/3.connect/SNS-04.png)

{{%notice tip%}}
After creat SNS we have the ARN SNS and also successfully connected Lambda2 as a trigger for DynamoDB Stream in the previous step. Now we update the code for Lambda2 to receive information from DynamoDB Stream and activate the customer booking confirmation email via SNS.
{{%/notice%}}

Okay we have created SNS and update code for Lambda2. Now we will move to the next step!



