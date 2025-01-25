---
title : "Creat DynamoDB"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---
This step is essential for storing and managing data for the serverless hotel booking chatbot. **DynamoDB**, a powerful NoSQL database service provided by AWS, is designed to handle large-scale queries with low latency. In this step, you need to create a DynamoDB table with appropriate primary keys to efficiently organize the data, such as tables for **ReservationID**, **Location**, **CheckInDate**, etc. Proper table design ensures optimal performance and scalability for the system.

Beside that, after creat DynamoDB table we also need to update code and Iam Roles policy for **Lambda1** we created before in order to connect smoothly to DynamoDB.


### Content:
   - [Creat DynamoDB](./3.3.1-creatdynamodb/)
   - [Update Lambda 1](./3.3.2-updatelambda1/)
 
