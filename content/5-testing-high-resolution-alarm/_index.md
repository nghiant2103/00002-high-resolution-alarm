---
title : "Testing high-resolution alarm"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : "<b>5. </b>"
---

#### Connect to your EC2 Instance

Use the private key associated with your EC2 instance to connect via SSH. Replace your-ec2-instance-public-ip with the public IP address or DNS of your EC2 instance and your-private-key.pem with the path to your private key file:

```
ssh -i "your-private-key.pem" ec2-user@your-ec2-instance-public-ip
```

#### Create RAM consumer file

1. Create the **ram-consumer.sh** file using your preferred text editor.

```bash
nano ram-consumer.sh
```

2. Paste the following into the file.

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

3. Grant **execute permission** to the file.

```bash 
chmod +x ram-consumer.sh
```

#### Run RAM consumer file

1. Run command.

```bash 
./ram-consumer.sh
```

2. Then enter `2m`.

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/001-testing-high-resolution-alarm.png)

#### Monitoring RAM metric

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/002-testing-high-resolution-alarm.png)

#### Alert messages

1. Email **alert message**.

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/003-testing-high-resolution-alarm.png)

2. Slack **alert message**.

![Testing high-resolution alarm](/images/5-testing-high-resolution-alarm/004-testing-high-resolution-alarm.png)

The configuration of the high-resolution alarm is now finalized. I trust that this guide will will help you in the future.
Next step, we will continue to the resource cleanup process.