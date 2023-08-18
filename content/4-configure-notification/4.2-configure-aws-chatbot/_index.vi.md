---
title : "Cấu hình AWS Chatbot"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : "<b>4.2 </b>"
---

AWS Chatbot là một công cụ mạnh mẽ hỗ trợ giao tiếp và cộng tác liền mạch trong môi trường AWS của bạn bằng cách tích hợp với các nền tảng trò chuyện phổ biến như Slack. Với AWS Chatbot, bạn có thể nhận thông báo, cảnh báo và cập nhật theo thời gian thực từ các dịch vụ AWS khác nhau trực tiếp trong kênh trò chuyện ưa thích của mình. Trong bước này, tôi sẽ hướng dẫn bạn quy trình cấu hình AWS Chatbot, cho phép bạn luôn cập nhật thông tin, cộng tác hiệu quả và thực hiện hành động nhanh chóng dựa trên thông báo bạn nhận được.

#### Truy cập AWS Chatbot

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/001-configure-aws-chatbot.png)

#### Cấu hình Chat client

1. Tại mục **Chat client** chọn **Slack**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/002-configure-aws-chatbot.png)

2. Chọn **Configure client**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/003-configure-aws-chatbot.png)

3. Chọn **Slack workspace** của bạn, rồi chọn **Allow**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/004-configure-aws-chatbot.png)

#### Cấu hình Slack channel

1. Chọn **Configure new channel**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/005-configure-aws-chatbot.png)

2. Tại mục **Configuration name**, nhập `cw-alarm-configuration`.
3. Chọn **channel** mà AWS Chatbot sẽ gửi thông báo đến.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/006-configure-aws-chatbot.png)

4. Tại mục **Role name**, nhập `AWSChatbot-role`.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/007-configure-aws-chatbot.png)

5. Chọn **Region** mà Topic **AlarmTopic** đã được tạo trong đó.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/008-configure-aws-chatbot.png)

6. Chọn **Topic**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/009-configure-aws-chatbot.png)

7. Chọn **Configure**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/010-configure-aws-chatbot.png)

#### Thêm AWS App vào Slack channel

1. Chọn **Add an App**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/011-configure-aws-chatbot.png)

2. Chọn **Add**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/012-configure-aws-chatbot.png)

#### Kiểm tra thông báo

1. Chọn **cw-alarm-configuration**.
2. Chọn **Send test message**.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/013-configure-aws-chatbot.png)

3. Tin nhắn đã được gửi thành công.

![Configure AWS Chatbot](/images/4-configure-notification/4.2-configure-aws-chatbot/014-configure-aws-chatbot.png)

Bước tiếp theo, chúng ta sẽ cập nhật **CloudWatch Alarm Notification**.