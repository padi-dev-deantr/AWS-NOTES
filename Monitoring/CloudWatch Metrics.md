# AWS CloudWatch Metrics Guide

Amazon CloudWatch Metrics is a part of the Amazon CloudWatch service that provides a data-driven view into the performance and behavior of your AWS resources.

## What is a Metric?

In CloudWatch, a metric represents a time-ordered set of data points. Each data point has a time-stamp and a value (like the CPUUtilization of an EC2 instance). These metrics can be aggregated over specified periods of time (like 1 minute, 5 minutes, or longer).

## Types of Metrics:

1. **Default Metrics**: Many AWS services provide default metrics. For example, EC2 provides CPUUtilization, NetworkPacketsIn, and many others. You don't have to do anything to get these metrics. They're provided automatically and free of charge.

2. **Custom Metrics**: You can publish your own metrics to CloudWatch using the AWS SDKs or CLI. This is useful when you want to collect data that isn't covered by the default metrics. For example, you could create a custom metric for the number of users currently logged into a web application.

## Working with Metrics:

- **Viewing Metrics**: You can view metrics through the AWS Management Console, CLI, or SDKs. You can also view them as a graph, making it easier to analyze patterns over time.

- **Publishing Metrics**: You can publish your own data to CloudWatch as custom metrics. This can be done by making a `PutMetricData` API call.

- **Retrieving Metrics**: To retrieve metrics from CloudWatch, you use the `GetMetricData` or `GetMetricStatistics` API operations.

- **Searching Metrics**: You can use the `ListMetrics` API operation to list the metrics available for a specific AWS service in your account.

- **Alarms**: You can create alarms on any of your CloudWatch metrics. These alarms can send notifications or automatically make changes to the resources you're monitoring when a threshold is breached.

- **Metric Math**: You can use metric math to query multiple CloudWatch metrics and use math expressions to create new time series based on these metrics.

- **Metric Aggregation**: CloudWatch can aggregate metrics across dimensions. For example, you can aggregate the CPUUtilization metric for all EC2 instances in a particular Auto Scaling group.

Remember, metrics are kept for 15 months, so you can get a view of how a particular metric has changed over time. This is helpful for understanding trends and patterns, and making more informed decisions. 

Also, CloudWatch Metrics is a regional service. It will only show metrics and data from the same region in which you're operating.