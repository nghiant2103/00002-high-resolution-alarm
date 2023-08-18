---
title : "Thử nghiệm High-Resolution Alarm"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : "<b>5. </b>"
---

#### Kết nối đến EC2 Instance của bạn

Sử dụng khóa riêng được liên kết với EC2 instance của bạn để kết nối thông qua SSH.Thay your-ec2-instance-public-ip bằng địa chỉ IP công cộng hoặc DNS của EC2 instance và your-private-key.pem bằng đường dẫn đến file khóa riêng của bạn:

```
ssh -i "your-private-key.pem" ec2-user@your-ec2-instance-public-ip
```

#### Tạo file tiêu thụ RAM

1. Tạo file **ram-consumer.sh** bằng trình soạn thảo văn bản ưa thích của bạn.

```bash
nano ram-consumer.sh
```

2. Dán đoạn mã sau vào file.

```bash
#!/bin/bash

echo "Provide sleep time in the form of NUMBER[SUFFIX]"
echo "   SUFFIX may be 's' for seconds (default), 'm' for minutes,"
echo "   'h' for hours, or 'd' for days."
read -p "> " delay

echo "begin allocating memory..."
for index in $(seq 1000); do
    value=$(seq -w -s '' $index $(($index + 100000)))
    eval array$index=$value
done
echo "...end allocating memory"

echo "sleeping for $delay"
sleep $delay
```

3. Cấp **quyền thực thi** cho file.

```bash 
chmod +x ram-consumer.sh
```

#### Chạy file tiêu thụ RAM

1. Chạy command.

```bash 
./ram-consumer.sh
```

2. Sau đó nhập `2m`.

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/001-testing-high-resolution-alarm.png)

#### Giám sát RAM metric

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/002-testing-high-resolution-alarm.png)

#### Tin nhắn cảnh báo

1. **Tin nhắn cảnh báo** đến Email.

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/003-testing-high-resolution-alarm.png)

2. **Tin nhắn cảnh báo** đến Slack.

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/004-testing-high-resolution-alarm.png)

Cấu hình của cảnh báo với độ phân giải cao hiện đã hoàn tất. Tôi tin rằng hướng dẫn này sẽ giúp ích cho bạn trong tương lai.
Bước tiếp theo, chúng ta sẽ tiếp tục quá trình dọn dẹp tài nguyên.