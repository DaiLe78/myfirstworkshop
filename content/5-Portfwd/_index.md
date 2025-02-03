---
title : "Test Chatbot on the Website"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

### First Test ChatBot
1. Test on website.
![lasttest](/images/5.fwd/test-01.jpg)
![lasttest](/images/5.fwd/test-02.jpg)
![lasttest](/images/5.fwd/test-03.jpg)

2. Check DynamoDB table to see if data is written to the database.
![lasttest](/images/5.fwd/lasttest-04.png)

3. DynamoDB Stream send the data to Lambda2 in order to trigger SNS to send booking confirmation email to customer.
![lasttest](/images/5.fwd/lasttest-05.png)

OKay seems like everything is working properly and smoothly!

Congratulations on completing the lab on how to build a serverless hotel booking Chatbot on AWS. Remember to perform resource cleanup to avoid unintended costs.
