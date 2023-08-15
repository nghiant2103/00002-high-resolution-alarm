---
title : "Chuẩn bị"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : "<b>2. </b>"
---

Amazon Web Services (AWS) cung cấp một bộ công cụ toàn diện để xây dựng và quản lý cơ sở hạ tầng đám mây. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn quy trình tạo Virtual Private Cloud (VPC) với 1 public subnet, sau đó khởi chạy một Amazon Elastic Compute Cloud (EC2) instance nằm trong public subnet trong VPC, tạo IAM (Identity and Access Management) để EC2 gửi dữ liệu tới Amazon CloudWatch. Sau đó cài đặt và cấu hình CloudWatch Agent cho phép bạn thu thập các chỉ số và nhật ký tùy chỉnh từ máy chủ EC2 instance của bạn và gửi chúng tới Amazon CloudWatch.

Mình có hướng dẫn chi tiết trong bài này [CloudWatch Agent](https://nghiant2103.github.io/00001-cloudwatch-agent).

Tổng quan kiến trúc sau khi bạn hoàn thành sẽ như sau:

![Preparing resources](/images/arc-cw-agent-main.png)

Sau khi chuẩn bị, chúng ta có metric sau:

{{% notice note %}}
Chúng ta sẽ sử dụng metric này để tạo cảnh báo với độ phân giải cao trong bước tiếp theo.
{{% /notice %}}

![Preparing resources](/images/2-preparation/001-preparation.png)

Bước tiếp theo, chúng tôi sẽ cấu hình CloudWatch Alarm để kích hoạt cảnh báo khi chỉ số RAM đạt đến mức cao.
