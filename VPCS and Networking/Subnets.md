# AWS Subnets Guide

## Introduction
A subnet, or subnetwork, is a segment of a larger network, divided for reasons such as improving network performance or applying different security policies. In the context of AWS, a subnet is a range of IP addresses in your VPC. 

## Types of Subnets

There are two types of subnets in AWS: Public and Private.

### Public Subnet

- If a subnet's traffic is routed to an internet gateway, the subnet is known as a public subnet.

- Instances in a public subnet can have a public IP address and can be accessed directly from the internet.

### Private Subnet

- If a subnet doesn't have a route to the internet gateway, the subnet is known as a private subnet.

- Instances in a private subnet can't be accessed directly from the internet.

- They can access the internet via a NAT gateway if internet access is needed.

## Creating a Subnet

1. Open the Amazon VPC console.
2. In the navigation pane, choose 'Subnets', 'Create subnet'.
3. Complete the 'Create Subnet' dialog box (specify VPC, name, availability zone, and IPv4 CIDR block).
4. Choose 'Yes, Create'.

## Configuring Subnet Settings

- For each subnet, you can modify its route table, associate network ACLs, and set Auto-assign IP settings.

## Deleting a Subnet

1. Open the Amazon VPC console.
2. In the navigation pane, choose 'Subnets'.
3. Select the subnet, choose 'Actions', 'Delete subnet'.
4. Choose 'Yes, Delete'.

Please Note: You can't delete a subnet that has instances running in it.

## Best Practices

- Always design your VPC with a plan for IP addressing and subnet strategy. Make sure you have enough room for growth.

- Use private subnets to add an extra layer of security for your applications.

- Use Network ACLs to add another layer of security to your subnets.

## Conclusion

In AWS, understanding and properly setting up your subnets is key to configuring your VPC correctly. A well-structured VPC allows your services to communicate with each other as needed, while also keeping your applications secure.