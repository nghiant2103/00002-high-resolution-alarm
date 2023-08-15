---
title : "Cập nhật CloudWatch Alarm Notification"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : "<b>4.3 </b>"
---

Amazon CloudWatch Alarms provide a mechanism for monitoring metrics and triggering actions when specific conditions are met. Configuring actions for CloudWatch alarms, such as sending notifications to Amazon SNS (Simple Notification Service), allows you to receive timely alerts about important events in your AWS environment. In this comprehensive guide, we will walk you through the process of updating the action of a CloudWatch alarm to send notifications via Amazon SNS.

#### Navigate to CloudWatch Alarm

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/001-update-cw-alarm.png)

#### Update Alarm Notification

1. Select **RAM Alarm** then click **Edit**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/002-update-cw-alarm.png)

2. Click on **Configure actions**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/003-update-cw-alarm.png)

3. Click on **Add notification**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/004-update-cw-alarm.png)

4. Select **Topic**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/005-update-cw-alarm.png)

5. Click on **Preview and create**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/006-update-cw-alarm.png)

6. Click on **Update alarm**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/007-update-cw-alarm.png)

The configuration for SNS and AWS Chatbot to send alerts through Email and Slack is now complete.