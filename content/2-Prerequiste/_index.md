---
title : "Preparation "
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

{{% notice info %}}
You need to create a VPC and IAM Roles with Policies to perform this lab.
{{% /notice %}}

To learn how to create VPC, you can refer to the lab:
  - [Creat a VPC](https://docs.aws.amazon.com/vpc/latest/userguide/create-vpc.html)
 
To build a secure serverless chatbot on AWS, we need to prepare a Virtual Private Cloud (VPC) for isolating resources and enabling private access to services. Additionally, setting up IAM Roles and Policies is essential to manage permissions, ensuring secure interactions between AWS services like Lambda, Lex, and DynamoDB.

### Content
  - [Prepare VPC ](2.1-createec2/)
  - [Create IAM Role](2.2-createiamrole/)
