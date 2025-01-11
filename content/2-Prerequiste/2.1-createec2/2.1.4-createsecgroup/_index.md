---
title : "Create security groups"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.1.3 </b> "
---

#### Create security groups

In this step, we will proceed to create the security groups used for our Lambda functions, DAX, OpenSearch and VPC Endpoints.

#### Create security group for 2 Lambda functions located in private subnet

1. Go to [VPC service management console](https://console.aws.amazon.com/vpc)
  + Click **Security Group**.
  + Click **Create security group**.

![SG](/images/2.prerequisite/019-createsg.png)

3. In the **Security group name** field, enter **SG Lambda**.
  + In the **Description** section, enter **SG Lambda**.
  + In the **VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![SG](/images/2.prerequisite/lambda-01.png)

4. Keep **Outbound rule**, drag the mouse to the bottom.
  + Click **Create security group**.

{{%notice tip%}}
As you can see, the security group we created to use for Lambda functions will not need to open traditional ports like port **22**.
{{%/notice%}}


#### Create a security group for Amazon DAX located in a private subnet

1. After successfully creating a security group for Lambda functions, click the Security Groups link to return to the Security groups list.

![SG](/images/2.prerequisite/dax-01.png)

2. Click **Create security group**.

3. In the **Security group name** field, enter **SG DAX**.
  + In the **Description** section, enter **SG DAX**.
  + In the **VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![SG](/images/2.prerequisite/dax-02.png)

4. Scroll down.
  + Add **Inbound rule** for **Type**: Custom TCP Rule, **Protocol**: TCP, **Port range**: 8111 (DAX default port), **Source**: SG Lambda 
  + Add **Outbound rule** and keep as default.
  + Click **Create security group**.

![SG](/images/2.prerequisite/dax-03.png)

{{%notice tip%}}
For Amazon DAX in the private subnet, Lambda functions will connect to DAX to cache before sending to DynamoDB, so we need to allow inbound connection from our Lambda functions to DAX through port 8111.
{{%/notice%}}

#### Create a security group for Amazon OpenSearch located in a private subnet

1. After successfully creating a security group for DAX, click the Security Groups link to return to the Security groups list.

![SG](/images/2.prerequisite/OS-01.png)

2. Click **Create security group**.

3. In the **Security group name** field, enter **SG OpenSearch**.
  + In the **Description** section, enter **SG OpenSearch**.
  + In the **VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![SG](/images/2.prerequisite/OS-02.png)

4. Scroll down.
  + Add **Inbound rule** for **Type**: HTTP, **Protocol**: TCP, **Port range**: 80, **Source**: SG Lambda 
  + Add **Outbound rule** and keep as default.
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
