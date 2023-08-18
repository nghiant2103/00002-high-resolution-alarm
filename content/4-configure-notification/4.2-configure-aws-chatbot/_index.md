---
title : "Configure AWS Chatbot"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : "<b>4.2 </b>"
---

AWS Chatbot is a powerful tool that facilitates seamless communication and collaboration within your AWS environment by integrating with popular chat platforms like Slack. With AWS Chatbot, you can receive real-time notifications, alerts, and updates from various AWS services directly in your preferred chat channel. In this comprehensive step-by-step guide, I'll walk you through the process of configuring AWS Chatbot, enabling you to stay informed, collaborate efficiently, and take swift actions based on the notifications you receive.

#### Navigate to AWS Chatbot

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/001-configure-aws-chatbot.png)

#### Configure Chat client

1. In **Chat client** select **Slack**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/002-configure-aws-chatbot.png)

2. Click on **Configure client**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/003-configure-aws-chatbot.png)

3. Select your **Slack workspace**, then click on **Allow**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/004-configure-aws-chatbot.png)

#### Configure Slack channel

1. Click on **Configure new channel**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/005-configure-aws-chatbot.png)

2. In **Configuration name** field, enter `cw-alarm-configuration`.
3. Select the **channel** that AWS Chatbot will send notifications to.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/006-configure-aws-chatbot.png)

4. In **Role name** field, enter `AWSChatbot-role`.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/007-configure-aws-chatbot.png)

5. Select the **Region** that Topic **AlarmTopic** has been created in.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/008-configure-aws-chatbot.png)

6. Select **Topic**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/009-configure-aws-chatbot.png)

7. Click on **Configure**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/010-configure-aws-chatbot.png)

#### Add AWS App to Slack channel

1. Click on **Add an App**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/011-configure-aws-chatbot.png)

2. Click on **Add**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/012-configure-aws-chatbot.png)

#### Test Notifications

1. Choose **cw-alarm-configuration**.
2. Click on **Send test message**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/013-configure-aws-chatbot.png)

3. The message was sent successfully.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/014-configure-aws-chatbot.png)

Next step we will update **CloudWatch Alarm Notification**.