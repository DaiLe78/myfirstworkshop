---
title : "Preparation "
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

{{% notice info %}}
You need to create a VPC and VPC Endpoints to perform this lab.
{{% /notice %}}

To learn how to create VPC, you can refer to the lab:
  - [Creat a VPC](https://docs.aws.amazon.com/vpc/latest/userguide/create-vpc.html)

To learn how to creat VPC Endpoints, you can refer to the lab:
  - [Creat VPC Endpoints](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpcEndpoint.html)
 
To build a secure serverless hotel booking chatbot on AWS, we need to prepare a Virtual Private Cloud (VPC) for isolating resources and enabling private access to services. Additionally, setting up VPC endpoints is essential to manage permissions and ensure secure interactions between AWS services like Lambda, SNS, CloudWatch and DynamoDB.

### Content
  - [Prepare VPC ](2.1-createec2/)
  - [Create VPC Endpoints](2.2-createiamrole/)
