---
title : "Create DynamoDB Stream"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 3.5. </b> "
---


#### Create DynamoDB Stream 
1. Go to [DynamoDB service management console](https://ap-southeast-2.console.aws.amazon.com/dynamodbv2/home)
  + Click on **Tables** on the left menu.
  + Click on **BookingHotel** table we created before.
  + Click on **Exports and streams**.
![DynamoDBstream](/images/3.connect/DynamoDBstream-01.png)
  + In the **DynamoDB Stream details** click on **Turn on**.
  + In the **View type** section choose **New image** then click on **Turn on stream**.
![DynamoDBstream](/images/3.connect/DynamoDBstream-02.png)

### Create trigger to Lambda2
2. Scroll down to **Trigger** section.
  + Click on **Create trigger**.
![DynamoDBstream](/images/3.connect/DynamoDBstream-03.png)
  + In the **Lambda function** section choose **Lambda2**.
  + Click on **Create trigger**.
![DynamoDBstream](/images/3.connect/DynamoDBstream-04.png)

Okay we have created DynamoDB Stream and invoke Lambda2 trigger every time an item is changed or add. Now we will move to the next step!



