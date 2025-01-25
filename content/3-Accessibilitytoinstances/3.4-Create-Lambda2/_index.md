---
title : "Create Lambda2"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 3.4. </b> "
---


#### Create Lambda2 function 
1. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Click **Creat Function**.
  + Choose **Author from scratch**.
  + In the **Function name** section enter **Lambda2**.
  + Choose language **Python 3.13**.
  + The rest remains default. Then click on **Create function**.

![Lambda2](/images/3.connect/Lambda2-01.png)

{{%notice tip%}}
We will update the code for Lambda2 later after creat DynamoDB Stream and SNS in the following step.
{{%/notice%}}

### Add more IAM Roles for Lambda2
2. Go to [IAM service management console](https://us-east-1.console.aws.amazon.com/iam/home)
  + Click on **Roles**.
  + Select **Lambda2 role**.
  + Add these roles: **LambdaSNSPublishInlinePolicy**, **ec2:CreateNetworkInterface**, **ec2:DescribeNetworkInterfaces**, **ec2:DeleteNetworkInterface**, **dynamodb:ListStreams**, **dynamodb:GetShardIterator**, **dynamodb:DescribeStream**, **dynamodb:GetRecords**.

{{%notice tip%}}
These **ec2 permissions** ensure that Lambda can automatically create, use, and delete Network Interfaces when running within a VPC. These **dynamodb permissions** ensure that Lambda can function efficiently as a consumer of DynamoDB Streams.
{{%/notice%}}

Okay we have created Lambda2 function. Now we will move to the next step!


