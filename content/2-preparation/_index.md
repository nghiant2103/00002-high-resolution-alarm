---
title : "Preparing resources"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : "<b>2. </b>"
---

Amazon Web Services (AWS) offers a comprehensive set of tools to build and manage cloud infrastructure. In this guide, we will walk through the process of creating a Virtual Private Cloud (VPC) with 1 public subnet, then launching an Amazon Elastic Compute Cloud (EC2) instance located in the public subnet within the VPC, creating an IAM (Identity and Access Management) role for EC2 to send data to Amazon CloudWatch. Then install and config CloudWatch Agent which allows you to collect custom metrics and logs from your EC2 instances servers and send them to Amazon CloudWatch.

I have detailed instructions in this article [CloudWatch Agent](https://nghiant2103.github.io/00001-cloudwatch-agent).

The architecture overview after you complete will be as follows:

![Preparing resources](/images/arc-cw-agent-main.png)

After preparing, we have the following metric:

{{% notice note %}}
We will use this metric to create high-resolution alarm in the next step.
{{% /notice %}}

![Preparing resources](/images/2-preparation/001-preparation.png)

Next step we will configuring a CloudWatch Alarm to trigger an alert when the RAM metric reaches a high level.