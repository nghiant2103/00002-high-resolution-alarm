---
title : "Cấu hình SNS"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : "<b>4.1 </b>"
---

Amazon Simple Notification Service (Amazon SNS) là một dịch vụ nhắn tin mạnh mẽ cho phép bạn gửi thông báo đến nhiều điểm cuối khác nhau, bao gồm cả địa chỉ email. Khi được tích hợp với Amazon CloudWatch, bạn có thể cấu hình cảnh báo của CloudWatch để kích hoạt thông báo của Amazon SNS, đảm bảo rằng bạn nhận được thông báo kịp thời qua email khi các điều kiện cụ thể được đáp ứng. Trong hướng dẫn từng bước này, chúng ta sẽ hướng dẫn bạn quy trình thiết lập thông báo email Amazon SNS và thêm SNS vào cảnh báo CloudWatch của bạn.

### Tạo topic
#### Truy cập Amazon SNS

1. Chọn **Topics**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/001-configure-sns.png)

2. Chọn **Create topic**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/002-configure-sns.png)

#### Tạo topic

1. Tại mục **Name**, nhập `AlarmTopic`.
2. Tại mục **Display name**, nhập `Alarm Topic`.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/003-configure-sns.png)

3. Chọn **Create topic**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/004-configure-sns.png)


### Tạo subscription

#### Truy cập Amazon SNS

1. Chọn **Subscriptions**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/005-configure-sns.png)

2 Chọn **Create subscription**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/006-configure-sns.png)

#### Tạo subscription

1. Chọn **Topic ARN**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/007-configure-sns.png)

2. Chọn **Email Protocol**

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/008-configure-sns.png)

3. Nhập **địa chỉ email của bạn** để nhận thông báo từ Amazon SNS..

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/009-configure-sns.png)

4. Chọn **Create subscription**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/010-configure-sns.png)

#### Xác nhận subcription

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/011-configure-sns.png)

#### Kiểm tra thông báo

1. Truy cập **AlarmTopic**.
2. Chọn **Publish message**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/012-configure-sns.png)

3. Nhập **Subject** và **Message body**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/013-configure-sns.png)

4. Chọn **Publish message**.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/014-configure-sns.png)

5. Tin nhắn đã được gửi thành công.

![Configure SNS](/images/4-configure-notification/4.1-configure-sns/015-configure-sns.png)

Bước tiếp theo chúng ta sẽ cấu hình AWS Chatbot.