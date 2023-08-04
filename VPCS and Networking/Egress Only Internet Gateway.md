# AWS Egress Only Internet Gateway

The Egress-Only Internet Gateway (EIGW) is a feature of Amazon VPC that provides outbound internet access for IPv6-enabled instances in your VPCs, preventing inbound traffic initiated by external entities. It's essentially the equivalent of a NAT gateway, but for IPv6 traffic.

## Basic Concepts

- **Egress-Only Internet Gateway:** A horizontally scalable, redundant, and highly available AWS managed component that provides outbound-only internet access for IPv6-enabled instances in your VPC.

## How to Set Up an Egress-Only Internet Gateway

Here are the basic steps to set up an Egress-Only Internet Gateway:

1. **Create an Egress-Only Internet Gateway:** You can do this in the AWS Management Console, AWS CLI, or through the AWS SDKs.

2. **Attach the Egress-Only Internet Gateway to Your VPC:** Once the EIGW is created, it needs to be associated with your VPC.

3. **Modify Route Tables:** Update your route tables to ensure traffic is directed to the EIGW.

## Exam Tips

- Egress-Only Internet Gateways provide outbound-only internet access for IPv6-enabled instances in your VPCs, and prevent the internet from initiating an IPv6 connection with your instances.

- The EIGW is stateful; it means changes made to the traffic as it exits the VPC are applied to the traffic as it re-enters the VPC.

- The EIGW does not support IPv4 traffic, it's designed specifically for IPv6 traffic. For IPv4, you should use a NAT gateway or NAT instances.

Example code to create an Egress-Only Internet Gateway and attach it to a VPC:

```bash
aws ec2 create-egress-only-internet-gateway --vpc-id vpc-abc
```

And to add a route to the main route table:

```bash
aws ec2 create-route --route-table-id rtb-abc --destination-ipv6-cidr-block ::/0 --egress-only-internet-gateway-id eigw-abc
```

