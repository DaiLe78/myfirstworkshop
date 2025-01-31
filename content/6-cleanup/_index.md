+++
title = "Clean up resources"
date = 2025
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

We will take the following steps to delete the resources we created in this exercise.

#### Delete Lambda Functions

1. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Click **Instances**.
  + Select all 3 Lambda functions.
  + Click **Actions**, then click **Delete**.

![Clean](/images/6.clean/01-clean.jpg)


#### Delete S3 bucket

2. Go to [S3 service management console](https://s3.console.aws.amazon.com/s3/home)
  + Click on the S3 bucket we created for this lab. 
  + Click **Empty**.
  + Enter **permanently delete**, then click **Empty** to proceed to delete the object in the bucket.
  + Click **Exit**.

3. After deleting all objects in the bucket, click **Delete**

![Clean](/images/6.clean/02-clean.jpg)

4. Enter the name of the S3 bucket, then click **Delete bucket** to proceed with deleting the S3 bucket.

#### Delete API Gateway

5. Go to [API Gateway service management console](https://aws.amazon.com/api-gateway/)
  + Click on **APIs**.
  + Select **My Rest API**.
  + Click **Delete**.

![Clean](/images/6.clean/03-clean.jpg)

#### Delete Amazon LEX

6. Go to [LEX service management console](https://ap-southeast-2.console.aws.amazon.com/lexv2/home)
  + Click on **Bots**.
  + Select **HotelBookingBot**.
  + Click **Actions**, then click **Delete**.

![Clean](/images/6.clean/04-clean.jpg)

#### Delete VPC Endpoints

7. Go to [VPC service management console](https://console.aws.amazon.com/vpc/home)
  + Click **Endpoints**.
  + Select the 3 endpoints we created for the lab including **sns-vpc-endpoint**, **dynamodb-vpc-endpoint**, **cloudwatch-vpc-endpoint**.
  + Click **Actions**.
  + Click **Delete VPC endpoints**.

![Clean](/images/6.clean/05-clean.jpg)

8. In the confirm box, enter **delete**.
  + Click **Delete** to proceed with deleting endpoints.

9. Click the refresh icon, check that all endpoints have been deleted before proceeding to the next step.

#### Delete VPC

Before delete **VPC** we need to delete **Subnets**, **Security Groups**, **NACL**, **Route Table** and **Network Interfaces** first.

10. Delete **Subnet VPC**
  + Go to **Subnets** section in the **VPC Dashboard**.
  + Select all 3 Subnet.
  + Click **Actions** then click **Delete subnet**.

![Clean](/images/6.clean/06-clean.jpg)

11. Delete **Security Groups**
  + Go to **Security Groups** section in the **VPC Dashboard**.
  + Select all security groups.
  + Click **Actions** then click **Delete security group**.

![Clean](/images/6.clean/07-clean.jpg)

12. Delete **NACL**
  + Go to **Network ACLs** section in the **VPC Dashboard**.
  + Select the NACL.
  + Click **Actions** then click **Delete network ACLs**.

![Clean](/images/6.clean/08-clean.jpg)

13. Delete **Route Table**
  + Go to **Route tables** section in the **VPC Dashboard**.
  + Select the route table.
  + Click **Actions** then click **Delete route table**.

![Clean](/images/6.clean/09-clean.jpg)

14. Delete **Network Interfaces**
  + Go to **Subnets** section in the **VPC Dashboard**.
  + Select all 4 network interfaces.
  + Click **Actions** then click **Delete**.

![Clean](/images/6.clean/10-clean.jpg)

15. Go to [VPC service management console](https://console.aws.amazon.com/vpc/home)
   + Click **Your VPCs**.
   + Click on **Lab VPC**.
   + Click **Actions**.
   + Click **Delete VPC**.

![Clean](/images/6.clean/11-clean.jpg)

#### Delete DynamoDB and DynamoDB Stream

16. Go to [DynamoDB service management console](https://ap-southeast-2.console.aws.amazon.com/dynamodbv2/home)
   + Click **Tables**.
   + Select **BookingHotel** table.
   + Click **Delete**.

![Clean](/images/6.clean/12-clean.jpg)

#### Delete SNS

17. Go to [SNS service management console](https://ap-southeast-2.console.aws.amazon.com/sns/v3/home)
   + Click **Topics**.
   + Select **MyLabSNS** topic.
   + Click **Delete**.

![Clean](/images/6.clean/13-clean.jpg)

#### Delete CloudWatch Logs, Metrics and Alarms

18. Go to [CloudWatch service management console](https://ap-southeast-2.console.aws.amazon.com/cloudwatch/home)
   + Click **Alarms**.
   + Select **LambdaErrorAlarm**.
   + Click **Actions**, then click **Delete**.

![Clean](/images/6.clean/14-clean.jpg)

  + Click **Log groups**.
  + Select all the log groups.
  + Click **Actions**, then click **Delete**.

![Clean](/images/6.clean/15-clean.jpg)

#### Delete IAM Roles

19. Go to [IAM service management console](https://us-east-1.console.aws.amazon.com/iam/home)
   + Click **Roles**.
   + Select 3 Lambda roles.
   + Click **Delete**.

![Clean](/images/6.clean/16-clean.jpg)
