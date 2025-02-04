---
title : "Create S3 Bucket and website interface"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1. </b> "
---


#### Create website interface 
1. We creat a website interface with chatbot with HTML, CSS and JavaScript.
I will put the source code under the following Github link.

[Source code Website](https://github.com/DaiLe78/Source-code-Chatbot-AWS)


{{%notice tip%}}
S3 Bucket will use this source code to host static website.
{{%/notice%}}

### Create S3 Bucket
2. Go to [S3 service management console](https://ap-southeast-2.console.aws.amazon.com/s3/home)
  + Click on **Create Bucket**.
  + In the **Bucket name** section enter **Mychatbot-website123**.
  + Untick the **Block all public access**.
![s3](/images/4.s3/s3-01.png)
  + The rest remain default. Then creat bucket.
  + Click on **Mychatbot-website123** and upload file code.
![s3](/images/4.s3/s3-02.png)
  + Go to **Properties Bucket** and enabled **S3 static website hosting**.
![s3](/images/4.s3/s3-03.png)
  + Go to **Edit Object Ownership** and choose **ACLs enabled**.
![s3](/images/4.s3/s3-04.png)
  + Go back to **Objects** and choose all the file uploaded. Click on **Actions** and choose **Make public using ACL**. 
![s3](/images/4.s3/s3-05.png)

{{%notice tip%}}
You have to ensure enabled **S3 static website hosting**, **ACLs enabled**, **Make publice using ACL** and untick **Block all public access** to be able to access our website on the Internet.
{{%/notice%}}

Okay we have created S3 Bucket to host static website. Now we will move to the next step!


