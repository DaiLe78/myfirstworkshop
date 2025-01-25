---
title : "Create CloudWatch Logs, Metrics and Alarms"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 3.7. </b> "
---


#### Create CLoudWatch Logs and Metrics for Lambda1

{{%notice tip%}}
We creat these CloudWatch for Lambda1 to track processing performance and detection of errors in Lambda's Backend code. 
{{%/notice%}}

1. Go to [Lambda service management console](https://ap-southeast-2.console.aws.amazon.com/lambda/home)
  + Scroll down to **Monitor** section.
  + Click on **View CloudWatch Logs**.
![CloudWatch](/images/3.connect/Cloudwatch-01.png)
  + Click on **Create metric filter**.
  + In **Step 1** part **Filter pattern** enter **ERROR**.
![CloudWatch](/images/3.connect/Cloudwatch-02.png)
  + In **Step 2** part **Filter name** enter **Lambda1ErrorFilter**, part **Metric namespace** enter **AWS/Lambda**.
  + Part **Metric name** enter **MyChatbotMetric**, part **Metric value** enter **1**.
![CloudWatch](/images/3.connect/Cloudwatch-03.png)
  + In **Step 3** review and create metric.
![CloudWatch](/images/3.connect/Cloudwatch-04.jpg)

### Create CloudWatch Alarm for Lambda1
2. Go to **CloudWatch Alarm** section.
  + Click on **Create alarm**.
  + In **Step 1** part **Metric name** enter **MyChatbotMetric**, part **Statistic** enter **Sum**, part **Period** enter **5 minutes**.
![CloudWatch](/images/3.connect/Cloudwatch-05.png)
  + In **Step 2** part **Alarm state trigger** choose **In alarm**, part **Send a notification to the following SNS topic** choose **Select an exsiting SNS topic** and then choose **MyLabSNS** we created before.

{{%notice tip%}}
This step we configure if there are more than 5 errors within 5 minutes, then send email notifications via SNS.
{{%/notice%}}
![CloudWatch](/images/3.connect/Cloudwatch-06.jpg)
  + In **Step 3** part **Alarm name** enter **LambdaErrorAlarm**.
  + In **Step 4** review and creat alarm.
![CloudWatch](/images/3.connect/Cloudwatch-07.jpg)

Okay we have created CloudWatch Logs, Metrics and Alarms. Now we will move to the next step!




