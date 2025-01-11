---
title : "Create Lambda Functions"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.1.4 </b> "
---

1. Go to [AWS Lambda Function console](https://ap-southeast-2.console.aws.amazon.com/lambda)
  + Click **Create a function**.
 
![EC2](/images/2.prerequisite/027-createec2.png)

2. Choose **Use a blueprint**.
  
![EC2](/images/2.prerequisite/028-createec2.png)

3. In the **Basic information** step.
 + In the **Blueprint name** section, choose **Manage orders with LEX** python 3.10 version.
 + In the **Function name** section, enter **Lambda1**.
 + In the **Execution role** section, creat a new role with **AWSLambdaBasicExecutionRole** and **AWSLambdaVPCAccessExecutionRole**.
 + Then click on **Creat function**
![EC2](/images/2.prerequisite/029-createec2.png)

4. In this step we will attach **VPC** and **Security Group** for **Lambda function 1**.
  + In the **Lambda1** we have just created, click on **Configuration**.
  + Then click on **VPC** in the left menu.
  ![EC2](/images/2.prerequisite/029-createec2.png)
  + In the **Edit VPC** section, click the **X** to reselect the **Lab VPC** you created for this lab.
  + In the **Subnet** section, click the **Lab Private Subnet** you created for this lab.
  + In the **Security Groups** section, click the **SG Lambda** you created for this lab.
  + Then scroll down and click on **Save**

![EC2](/images/2.prerequisite/030-createec2.png)

5. Click **Next: Add Tags** to move to the next step.
  + Click **Next: Configure Security Group** to move to the next step.


6. On page **Step 6: Configure Security Group**.
  + Select **Select an existing security group**.
  + Select security group **SG Public Linux Instance**.
  + Click **Review and Launch**.

![EC2](/images/2.prerequisite/031-createec2.png)

7. The warning dialog box appears because we do not configure the firewall to allow connections to port 22, Click **Continue** to continue.

8. At page **Step 7: Review Instance Launch**.
  + Click **Launch**.

9. In the **Select an existing key pair or create a new key pair** dialog box.
  + Click to select **Create a new key pair**.
  + In the **Key pair name** field, enter **LabKeypair**.
  + Click **Download Key Pair** and save it to your computer.
  + Click **Launch Instances** to create EC2 server.

![EC2](/images/2.prerequisite/032-createec2.png)

10. Click **View Instances** to return to the list of EC2 instances.

11. Click the edit icon under the **Name** column.
  + In the **Edit Name** dialog box, enter **Public Linux Instance**.
  + Click **Save**.

![EC2](/images/2.prerequisite/033-createec2.png)

Next, we will do the same to create an EC2 Instance Windows running in the Private subnet.
