---
title : "Dọn dẹp tài nguyên"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : "<b>6. </b>"
---

Chúng ta sẽ thực hiện các bước sau để xóa các tài nguyên mà chúng ta đã tạo trong workshop này.

#### Xóa EC2 instance

- Truy cập [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
  + Chọn **Instances**.
  + Chọn **server** instance.
  + Chọn **Instance state**.
  + Chọn **Terminate instance**, rồi chọn **Terminate** để xác nhận.

![Cleanup](/images/6-cleanup/001-cleanup.png)

#### Xóa IAM Role

- Truy cập [IAM service management console](https://console.aws.amazon.com/iamv2/home#/home)
  + Chọn **Roles**.
  + Trong search box, nhập `EC2CWAgentRole`.
  + Chọn **EC2CWAgentRole**.
  + Chọn **Delete**, rồi nhập tên role **EC2CWAgentRole** và chọn **Delete** để xóa role.

![Cleanup](/images/6-cleanup/002-cleanup.png)

#### Xóa VPC

1. Truy cập [VPC service management console](https://console.aws.amazon.com/vpc/home)
    + Chọn **Your VPCs**.
    + Chọn **cw-agent-vpc**.
    + Chọn **Actions**.
    + Chọn **Delete VPC**.

2. Trong confirm box, nhập **delete** để xác nhận, chọn **Delete** để xóa **cw-agent-vpc** và các tài nguyên liên quan.

![Cleanup](/images/6-cleanup/003-cleanup.png)

#### Xóa Alarm

![Cleanup](/images/6-cleanup/004-cleanup.png)

#### Xóa Slack workspace

1. Xóa configurations.

![Cleanup](/images/6-cleanup/005-cleanup.png)

2. Xóa cấu hình workspace.

![Cleanup](/images/6-cleanup/006-cleanup.png)

#### Xóa SNS Topic và Subscription

1. Xóa **Subscription**.

![Cleanup](/images/6-cleanup/007-cleanup.png)

2. Xóa **Topic**.

![Cleanup](/images/6-cleanup/008-cleanup.png)
