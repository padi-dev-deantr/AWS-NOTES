# AWS CloudWatch

Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on AWS. You can use CloudWatch to collect and track metrics, collect and monitor log files, set alarms, and automatically react to changes in your AWS resources.

## 1. [[AWS/Monitoring/CloudWatch Metrics|CloudWatch Metrics]]

CloudWatch provides metrics for every service in AWS. These are the variables it measures for a resource (like CPUUtilization for EC2 instances, or NumberOfMessagesSent for SQS). You can also create and send your custom metrics to CloudWatch.

Some metrics are available by default like CPU usage of EC2 instances, while others may need to be explicitly enabled, like memory usage.

## 2. [[CloudWatch Alarms]]

You can create alarms based on any of your metrics to send notifications or even automate actions if a metric reaches a threshold you set. For instance, if CPU Utilization is above 90% for a certain period of time, you could get a notification, or trigger an Auto Scaling policy to add more instances.

## 3. Dashboard

CloudWatch Dashboards are customizable home pages in the CloudWatch console that you can use to monitor your resources in a single view, even those spread across different regions.

## 4. Logs

CloudWatch Logs help you to aggregate, monitor, and store logs. AWS services can send logs directly to CloudWatch. You can also send your custom logs from your application using AWS SDKs or CloudWatch agent.

## 5. Events

CloudWatch Events delivers a near real-time stream of system events that describe changes in AWS resources. Using simple rules that you can quickly set up, you can match events and route them to one or more target functions or streams.

## 6. Anomaly Detection

CloudWatch Anomaly Detection applies machine-learning algorithms to continuously analyze system and application metrics, determine a normal baseline, and surface anomalies with minimal user intervention.

## 7. ServiceLens

AWS CloudWatch ServiceLens is a feature that enables you to visualize and analyze the health, performance, and availability of your applications in a single place.

## 8. Contributor Insights

CloudWatch Contributor Insights helps you analyze log data and create time series that displays top contributors impacting system performance.

Remember, CloudWatch is regional, so if you want to create a global dashboard across regions, you'll need to use CloudWatch cross-region dashboards. Also, keep in mind the costs associated with detailed monitoring, CloudWatch Logs, and custom metrics.