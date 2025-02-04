---
title : "Create Lambda Connect API Gateway to Lex"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2. </b> "
---


#### Create LambdaConnectAPIgwToLex function 
1. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Click **Creat Function**.
  + Choose **Author from scratch**.
  + In the **Function name** section enter **LambdaCoonectAPIgwToLex**.
  + Choose language **Python 3.13**.
  + The rest remains default. Then click on **Create function**.
![lambdaconnect](/images/4.s3/lambdaconnect.png)
  + Replace the default Lambda code with this code. I will put the source code under the following GitHub link.

[Source code LambdaConnectAPIgwToLex](https://github.com/DaiLe78/Source-code-Chatbot-AWS/blob/master/LambdaConnectAPIgwToLex.py)


### Add more IAM Roles for Lambda2
2. Go to [IAM service management console](https://us-east-1.console.aws.amazon.com/iam/home)
  + Click on **Roles**.
  + Select **LambdaConnectAPIgwToLex role**.
  + Add **AmazonLexFullAccess** role.


Okay we have created LambdaConnect function. Now we will move to the next step!



