---
title : "Preparing VPC and Security Groups"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

In this step, we will need to create a VPC with 3 private subnets. Then create security groups for 2 Lambda functions and VPC Endpoints. Lastly we creat VPC Endpoints for SNS, DynamoDB and CloudWatch.

The architecture overview after you complete this step will be as follows:

![VPC](/images/image.png)




### Content
  - [Create VPC](2.1.1-createvpc/)
  - [Create Private Subnet](2.1.2-createprivatesubnet/)
  - [Create security group](2.1.3-createsecgroup/)
