# VPC Flow Logs

VPC Flow Logs is a feature that enables you to capture information about the IP traffic going to and from network interfaces in your VPC. Flow logs can be created at three levels: VPC, Subnet, and Network Interface Level.

Flow logs data can be used to troubleshoot why specific traffic is not reaching an instance, or to monitor the traffic that is reaching your instance.

## Basic Concepts

- **Flow Logs:** Records of network traffic in your VPC, which are stored using Amazon CloudWatch Logs.

- **Aggregation Levels:** Flow logs can be created at the VPC, subnet, or network interface level.

- **Log Format:** Each record captures specific metadata about the IP traffic, but not the actual content of the traffic.

## Creating VPC Flow Logs

You can set up VPC Flow Logs through the AWS Management Console, AWS CLI, or AWS SDKs. Here's a basic step-by-step guide for creating flow logs using the AWS Management Console:

1. Open the Amazon VPC console.

2. In the navigation pane, choose 'Your VPCs', 'Subnets', or 'Network Interfaces'.

3. Select the VPC, subnet, or network interface for which to create a flow log.

4. Choose 'Actions', 'Create flow log'.

5. In the 'Create flow log' dialog box, configure the flow log. Specify the following details:
   - **Filter:** You can choose to log all traffic, or just accepted or rejected traffic.
   - **Destination Log Group:** The name of a new or existing CloudWatch Logs log group where the flow logs are to be published.
   - **IAM Role:** The IAM role that has permissions to publish flow logs to the log group.
   - **Format:** The format of the flow logs.

6. Choose 'Create Flow Log'.

## Exam Tips

- VPC Flow Logs do not capture real-time log streams. There can be a delay of about 10 minutes between the time a log is created and the time it appears in CloudWatch.

- VPC Flow Logs do not capture traffic to or from the metadata service (169.254.169.254), DNS traffic, or DHCP traffic. They also do not capture traffic between instances and reserved IP addresses for AWS such as Amazon S3.

- If you have created a VPC Flow Log, and then you delete your VPC or subnet, or you deregister the network interface, the flow logs data will also be deleted and cannot be recovered.

- VPC Flow Logs incurs costs for data ingestion and data archiving in CloudWatch.