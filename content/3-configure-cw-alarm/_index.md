---
title : "Configure CloudWatch Alarm"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : "<b>3. </b>"
---

Amazon CloudWatch provides a comprehensive monitoring solution for your AWS resources, allowing you to gain insights into their performance, health, and operational status. One essential feature of CloudWatch is the ability to create alarms that notify you when specific thresholds are breached. In this step-by-step guide, we will walk you through the process of configuring CloudWatch alarms to enhance your monitoring strategy and ensure timely notifications for critical events.

#### Navigate to AWS CloudWatch
- Choose **All alarms**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/001-configure-cw-alarm.png)

#### Create a new alarm

- Click on **Create alarm**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/002-configure-cw-alarm.png)

#### Select metric

1. Click on **Select metric**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/003-configure-cw-alarm.png)

2. In **Custom namespaces** section, click on **WorkshopCWAgent**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/004-configure-cw-alarm.png)

3. Click on **InstanceID**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/005-configure-cw-alarm.png)

4. Select RAM metric.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/006-configure-cw-alarm.png)

5 Click on **Select metric**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/007-configure-cw-alarm.png)

#### Period

- Select period 10s.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/008-configure-cw-alarm.png)

#### Conditions

- Configure alarm condition.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/009-configure-cw-alarm.png)

#### Notification

- Remove Notification configure, we will configure later.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/010-configure-cw-alarm.png)

#### Alarm name

- In the **Alarm name** field, enter `RAM Alarm`.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/011-configure-cw-alarm.png)

#### Preview and create alarm

- Review the alarm configuration, then click on Create alarm.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/012-configure-cw-alarm.png)

#### Alarm status

- During the initial few minutes, the state may display **Insufficient** data.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/013-configure-cw-alarm.png)

- However, it will display **OK** shortly thereafter.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/014-configure-cw-alarm.png)

In the upcoming step, we will set up the configuration for SNS and AWS Chatbot to send alerts via Email and Slack.