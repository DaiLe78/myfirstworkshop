---
title : "Create Security Groups"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.1.3 </b> "
---

#### Create Security Groups

In this step, we will proceed to create the security groups used for our Lambda functions and VPC Endpoints.

#### Create security group for Lambda 1 located in private subnet

1. Go to [VPC service management console](https://console.aws.amazon.com/vpc)
  + Click **Security Group**.
  + Click **Create security group**.

![SG](/images/2.prerequisite/019-createsg.png)

3. In the **Security group name** field, enter **SG Lambda1**.
  + In the **Description** section, enter **sg for lambda1**.
  + In the **VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![SG](/images/2.prerequisite/lambda-01.png)

4. Keep **Inbound rule** blank, **Outbound rule** allows **All traffic**.

![SG](/images/2.prerequisite/lambda-02.png)

5. Drag the mouse to the bottom.
  + Click **Create security group**.

#### Create security group for Lambda 2 located in private subnet

{{%notice tip%}}
We configure the same as lambda 1 but now leave both the inbound and outbound rule blank. We will add these rules later!
{{%/notice%}}

#### Create a security group for VPC Endpoint for SNS

1. After successfully creating a security group for Lambda functions, click the Security Groups link to return to the Security groups list.

2. Click **Create security group**.

3. In the **Security group name** field, enter **SG VPC Endpoint For SNS**.
  + In the **Description** section, enter **sg vpc endpoint for sns**.
  + In the **VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![SG](/images/2.prerequisite/SG-VPCE-SNS-01.png)

4. Scroll down.
  + Add **Inbound rule** for **Type**: All traffic, **Protocol** and **Port range**: All, **Source**: SG Lambda 2 
  + Add **Outbound rule** and keep as blank.
  + Click **Create security group**.

![SG](/images/2.prerequisite/SG-VPCE-SNS-02.png)

#### Create a security group for VPC Endpoint for DynamoDB

1. After successfully creating a security group for VPC Endpoint for SNS, click the Security Groups link to return to the Security groups list.

2. Click **Create security group**.

3. In the **Security group name** field, enter **SG VPC Endpoint For DynamoDB**.
  + In the **Description** section, enter **sg vpc endpoint for dynamodb**.
  + In the **VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![SG](/images/2.prerequisite/SG-VPCE-DynamoDB-01.png)

4. Scroll down.
  + Add **Inbound rule** for **Type**: All traffic, **Protocol** and **Port range**: All, **Source**: SG Lambda 1 
  + Keep **Outbound rules** as blank.
  + Click **Create security group**.

![SG](/images/2.prerequisite/OS-03.png)

{{%notice tip%}}
For OpenSearch in the private subnet we need to allow inbound connection from our Lambda functions to OpenSearch through port 80.
{{%/notice%}}

#### Create security group for VPC Endpoint

1. In this step, we will create security group for VPC Endpoint.
2. After successfully creating the security group for OpenSearch in the private subnet, click the Security Groups link to return to the Security groups list.
3. Click **Create security group**.
4. In the **Security group name** field, enter **SG VPC Endpoint**.
  + In the **Description** section, enter **SG VPC Endpoint**.
  + In the **VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![SG](/images/2.prerequisite/VPCE-01.png)

5. Scroll down.
  + Add **Outbound rule** as default.

6. Add **Inbound rule** allowing TCP 443 to come from 10.10.0.0/16 ( CIDR of **Lab VPC** we created ).
  + Click **Create security group**.

![SG](/images/2.prerequisite/VPCE-02.png)

So we are done creating the necessary security groups for Lambda functions, DAX, OpenSearch and VPC Endpoints.
