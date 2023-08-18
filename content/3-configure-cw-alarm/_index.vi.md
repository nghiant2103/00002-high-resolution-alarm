---
title : "Cấu hình CloudWatch Alarm"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : "<b>3. </b>"
---

Amazon CloudWatch cung cấp giải pháp giám sát toàn diện cho các tài nguyên AWS của bạn, cho phép bạn hiểu rõ hơn về hiệu suất, tình trạng và trạng thái hoạt động của chúng. Một tính năng thiết yếu của CloudWatch là khả năng tạo cảnh báo để thông báo cho bạn khi các ngưỡng cụ thể bị vi phạm. Trong bước này, tôi sẽ hướng dẫn bạn quy trình cấu hình cảnh báo CloudWatch để nâng cao chiến lược giám sát của bạn và đảm bảo thông báo kịp thời cho các sự kiện quan trọng.

#### Truy cập AWS CloudWatch
- Chọn **All alarms**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/001-configure-cw-alarm.png)

#### Tạo một cảnh báo mới

- Chọn **Create alarm**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/002-configure-cw-alarm.png)

#### Chọn metric

1. Chọn **Select metric**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/003-configure-cw-alarm.png)

2. Trong phần **Custom namespaces**, chọn **WorkshopCWAgent**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/004-configure-cw-alarm.png)

3. Chọn **InstanceID**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/005-configure-cw-alarm.png)

4. Chọn RAM metric.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/006-configure-cw-alarm.png)

5 Chọn **Select metric**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/007-configure-cw-alarm.png)

#### Period

- Chọn period 10s.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/008-configure-cw-alarm.png)

#### Conditions

- Cấu hình điều kiện cảnh báo.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/009-configure-cw-alarm.png)

#### Notification

- Bỏ cấu hình Notification đi, chúng ta sẽ cấu hình sau.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/010-configure-cw-alarm.png)

#### Tên cảnh báo

- Tại mục **Alarm name**, nhập `RAM Alarm`.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/011-configure-cw-alarm.png)

#### Xem trước và tạo cảnh báo

-  Xem lại cấu hình cảnh báo, rồi chọn Create alarm.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/012-configure-cw-alarm.png)

#### Trạng thái cảnh báo

- Trong vài phút đầu tiên, trạng thái có thể hiển thị dữ liệu **Insufficient**.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/013-configure-cw-alarm.png)

- Tuy nhiên, nó sẽ hiển thị **OK** ngay sau đó.

![Configure CloudWatch Alarm](/images/3-configure-cw-alarm/014-configure-cw-alarm.png)

Trong bước tiếp theo, chúng ta sẽ thiết lập cấu hình cho SNS và AWS Chatbot để gửi cảnh báo qua Email và Slack.