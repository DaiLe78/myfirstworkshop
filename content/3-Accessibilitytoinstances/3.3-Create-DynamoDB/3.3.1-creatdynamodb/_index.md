---
title : "Create DynamoDB"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.3.1 </b> "
---


#### Create DynamoDB table 
1. Go to [DynamoDB service management console](https://ap-southeast-2.console.aws.amazon.com/dynamodbv2/home)
  + Click **Creat Table**.
  + In the **Table name** section enter **BookingHotel**.
  + In the **Partition key** section enter **ReservationID** and type **String**.
  + The rest remains default. Then click on **Create Tbale**.

![DynamoDB](/images/3.connect/DynamoDB-01.png)

2. Click on **BookingHotel** table we created.
  + Click on **Explore items**.
  + Click on **Create items**.
  + Beside **ReservationID** create more 5 keys : **Location**, **CheckInDate**, **Nights**, **RoomType**, **Timestamp** and **Email**. Give them some demo value like the picture bellow. 

![DynamoDB](/images/3.connect/DynamoDB-02.png)

Okay now we will update our Lambda1!
