---
title : "Add Lambda1 and Lambda2 into LabVPC"
date : "`r Sys.Date()`"
weight : 8
chapter : false
pre : " <b> 3.8. </b> "
---


### Add Lambda1 into LabVPC
1. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Click on **Configuration** section.
![AddVPC](/images/3.connect/Addvpc-01.jpg)
  + Click on **Edit**.
  + In the **VPC** section choose our **LabVPC**.
  + In the **Subnet** section choose subnets in VPC.
  + In the **Security groups** choose **SG Lambda1** we created before.
![AddVPC](/images/3.connect/Addvpc-02.jpg)

### Add Lambda2 into LabVPC

{{%notice tip%}}
We take the same steps as with Lambda1.
{{%/notice%}}

Now we have added 2 Lambda functions into our LabVPC to increase security. Through 3 VPC Endpoints we created before, Lambda1 in VPC will be able to connect to CloudWatch and DynamoDB, Lambda2 in VPC will be able to connect to SNS.



