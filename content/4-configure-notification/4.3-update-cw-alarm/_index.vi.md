---
title : "Cập nhật CloudWatch Alarm Notification"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : "<b>4.3 </b>"
---

Amazon CloudWatch Alarms cung cấp một cơ chế để giám sát các metric và kích hoạt action khi các điều kiện cụ thể được đáp ứng. Việc cấu hình các action cho cảnh báo CloudWatch, chẳng hạn như gửi thông báo tới Amazon SNS (Simple Notification Service), cho phép bạn nhận cảnh báo kịp thời về các sự kiện quan trọng trong môi trường AWS của mình. Trong hướng dẫn toàn diện này, tôi sẽ hướng dẫn bạn quy trình cập nhật action của cảnh báo CloudWatch để gửi thông báo qua Amazon SNS.

#### Truy cập CloudWatch Alarm

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/001-update-cw-alarm.png)

#### Cập nhật Alarm Notification

1. Chọn **RAM Alarm** rồi chọn **Edit**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/002-update-cw-alarm.png)

2. Chọn **Configure actions**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/003-update-cw-alarm.png)

3. Chọn **Add notification**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/004-update-cw-alarm.png)

4. Chọn **Topic**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/005-update-cw-alarm.png)

5. Chọn **Preview and create**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/006-update-cw-alarm.png)

6. Chọn **Update alarm**.

![Update CloudWatch Alarm Notification](/images/4-configure-notification/4.3-update-cw-alarm/007-update-cw-alarm.png)

Cấu hình cho SNS và AWS Chatbot để gửi cảnh báo qua Email và Slack đã hoàn tất.