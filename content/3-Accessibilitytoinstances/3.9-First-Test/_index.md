---
title : "First Test ChatBot"
date : "`r Sys.Date()`"
weight : 9
chapter : false
pre : " <b> 3.9. </b> "
---


### First Test ChatBot
1. Test Amazon LEX and Lambda1 processing logic code.
![firsttest](/images/3.connect/first-test-01.png)
![firsttest](/images/3.connect/first-test-02.png)
![firsttest](/images/3.connect/first-test-03.png)

2. Check DynamoDB table to see if data is written to the database.
![firsttest](/images/3.connect/first-test-04.png)

3. DynamoDB Stream send the data to Lambda2 in order to trigger SNS to send booking confirmation email to customer.
![firsttest](/images/3.connect/first-test-05.png)

4. Case if the customer makes a booking where there are no hotel facilities there.
![firsttest](/images/3.connect/first-test-06.png)

OKay seems like everything is working properly and smoothly. Next we will integrate Chatbot on the website!




