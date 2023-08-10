# AWS CloudWatch Logs Guide

Amazon CloudWatch Logs is a feature of CloudWatch that allows you to collect, monitor, and store logs from your resources in near real-time. These logs can be used for debugging, auditing, or analysing the usage patterns of your applications.

## Collecting Logs

- **Amazon EC2 Instances**: You can use the CloudWatch Logs agent to send log data from your applications to CloudWatch Logs.
  
- **AWS CloudTrail**: You can send trails of AWS API calls from CloudTrail to CloudWatch Logs.
  
- **AWS Lambda**: You can send logs from your Lambda functions to CloudWatch Logs.

- **VPC Flow Logs**: You can publish flow logs data to CloudWatch Logs and view them to monitor the IP traffic to and from the network interfaces in your VPC.

- **Amazon ECS**: Docker logs from ECS containers can be sent to CloudWatch Logs.

- **Other AWS services**: Many AWS services integrate with CloudWatch Logs. They either send logs automatically or have configuration options to enable log delivery to CloudWatch Logs.

## Working with Logs

- **Viewing Logs**: You can view your logs in the CloudWatch console. Logs are grouped into Log Groups and Log Streams. Log Groups represent a collection of log streams that share the same retention, monitoring, and access control settings. Log Streams represent a sequence of log events that share the same source.

- **Searching Logs**: Within a Log Group, you can filter the logs using specific text patterns, terms, or phrases.

- **Log Retention**: By default, logs are kept indefinitely. However, you can adjust the retention setting for each Log Group, specifying how long to keep logs.

- **Exporting Logs**: You can export logs to an S3 bucket for long-term retention or analysis with other systems.

- **Alarms and Monitoring**: You can create metric filters to turn log data into numerical CloudWatch metrics that you can graph or set an alarm on. If a metric filter finds one of the terms or phrases in your logs, CloudWatch counts it, enabling you to use this count to create alarms.

- **Log Insights**: CloudWatch Log Insights enables you to interactively search and analyze your log data. It provides sample queries, command descriptions, query auto-completion, and log field discovery.

Using CloudWatch Logs, you can gain valuable insights from your log data and react to operational issues faster, thereby improving the overall performance and availability of your applications.
