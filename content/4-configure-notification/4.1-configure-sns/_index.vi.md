---
title : "Cấu hình SNS"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : "<b>4.1 </b>"
---

Amazon Simple Notification Service (Amazon SNS) is a powerful messaging service that enables you to send notifications to various endpoints, including email addresses. When integrated with Amazon CloudWatch, you can configure CloudWatch alarms to trigger Amazon SNS notifications, ensuring that you receive timely email alerts when specific conditions are met. In this step-by-step guide, we'll walk you through the process of setting up Amazon SNS email notifications and adding SNS actions to your CloudWatch alarms.

### Create topic
#### Navigate to Amazon SNS

1. Click on **Topics**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/001-configure-sns.png)

2. Click on **Create topic**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/002-configure-sns.png)

#### Create topic

1. In the **Name** field, enter `AlarmTopic`.
2. In the **Display name** field, enter `Alarm Topic`.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/003-configure-sns.png)

3. Click on **Create topic**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/004-configure-sns.png)


### Create subscription

#### Navigate to Amazon SNS

1. Choose **Subscriptions**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/005-configure-sns.png)

2 Click on **Create subscription**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/006-configure-sns.png)

#### Create subscription

1. Choose **Topic ARN**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/007-configure-sns.png)

2. Choose **Email Protocol**

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/008-configure-sns.png)

3. Enter **your email address** that can receive notifications from Amazon SNS.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/009-configure-sns.png)

4. Click on **Create subscription**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/010-configure-sns.png)

#### Comfirm subcription

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/011-configure-sns.png)

#### Test Notifications

1. Navigate to **AlarmTopic**.
2. Choose **Publish message**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/012-configure-sns.png)

3. Enter **Subject** and **Message body**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/013-configure-sns.png)

4. Click on **Publish message**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/014-configure-sns.png)

5. The message was sent successfully.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/015-configure-sns.png)

Next step we will configuring AWS Chatbot.