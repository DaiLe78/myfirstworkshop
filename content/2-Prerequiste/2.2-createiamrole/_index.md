---
title : "Create VPC Endpoints"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Create VPC Endpoints

In this step, we will proceed to create 3 VPC Endpoints for SNS, DynamoDB and CLoudWatch.

### Create VPC Endpoint For SNS

1. Go to **Private Link and Lattice** section on the left menu. Select on **Endpoint** section. Then click on **Creat Endpoint**.

![endpoint](/images/2.prerequisite/VPCE-SNS-01.png)

2. In the **name tag** section enter: sns-vpc-enpoint. In the **Type** section click on **AWS services**.

![endpoint](/images/2.prerequisite/VPCE-SNS-02.png)

3. In the **Services** choose **sns** type **interface**. In the **Network settings** section, click the **X** to reselect the **Lab VPC** you created for this lab.

![endpoint](/images/2.prerequisite/VPCE-SNS-03.png)

4. In the **Subnets** section, choose subnet on Availability Zone **2a** and IP address type **IPv4**.

![endpoint](/images/2.prerequisite/VPCE-SNS-04.png)

5. In the **Security groups** section, click on **SG VPC Endpoint For SNS** we have created before.

![endpoint](/images/2.prerequisite/VPCE-SNS-05.png)

6. Scroll down and click on **Creat Endpoint**.

### Create VPC Endpoint For DynamoDB and CloudWatch

{{%notice tip%}}
We do the same steps as VPC Endpoint For SNS above.
{{%/notice%}}

So we are done creating 3 VPC Endpoints for AWS Services.
