---
title : "Update code and IAM Roles policy for Lambda1"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.3.2 </b> "
---


#### Update code for Lambda1 
1. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Click on **Lambda1** function.
  + Scroll dowm to **Code Source** section.
  + Replace the default Lambda code with this code. I will put the source code under the following GitHub link:
    
    [Source code Lambda1](https://github.com/DaiLe78/Source-code-Chatbot-AWS/blob/master/Lambda1.py)

{{%notice tip%}}
This code for Lambda1 will handle the backend logic for Amazon Lex and connect Lambda1 to the DynamoDB table.
{{%/notice%}}

### Add more IAM Roles for Lambda1
2. Go to [IAM service management console](https://us-east-1.console.aws.amazon.com/iam/home).
  + Click on **Roles**.
  + Select **Lambda1 role**.
  + Add these roles: **AmazonDynamoDBFullAccess**, **ec2:CreateNetworkInterface**, **ec2:DescribeNetworkInterfaces**, **ec2:DeleteNetworkInterface**.

{{%notice tip%}}
These **ec2 permissions** ensure that Lambda can automatically create, use, and delete Network Interfaces when running within a VPC. They enable Lambda to connect to VPC resources, maintain performance, and manage network resources efficiently.
{{%/notice%}}



