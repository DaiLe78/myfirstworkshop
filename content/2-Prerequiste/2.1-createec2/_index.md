---
title : "Preparing VPC, Lambda, DAX and OpenSearch"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

In this step, we will need to create a VPC with 2 private subnets. Then create 2 Lambda functions, 1 Amazon DAX and 1 OpenSearch located in the private subnet.

The architecture overview after you complete this step will be as follows:

![VPC](/images/image1.png)




### Content
  - [Create VPC](2.1.1-createvpc/)
  - [Create Private Subnet](2.1.2-createprivatesubnet/)
  - [Create security group](2.1.4-createsecgroup/)
  - [Create public Linux server](2.1.5-createec2linux/)
  - [Create private Windows server](2.1.6-createec2windows/)
