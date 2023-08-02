# AWS VPC Endpoints

## Overview

A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, a NAT device, VPN, or firewall proxies.

There are two types of VPC endpoints:
- Interface Endpoints (powered by AWS PrivateLink)
- Gateway Endpoints

## Interface Endpoints

- An elastic network interface (ENI) with a private IP address serves as an entry point for traffic destined to a service or VPC endpoint service.
- It provides private connectivity to services across different AWS accounts and within other VPCs.
- Supported by many AWS services including API Gateway, CloudFormation, CloudTrail, CodeBuild, KMS, SageMaker, Secrets Manager, SQS, and others.

## Gateway Endpoints

- A gateway endpoint is a gateway that is a target for a specified route in your route table, used for traffic destined to either Amazon S3 or DynamoDB.
- Currently, only Amazon S3 and DynamoDB are supported by gateway endpoints.
- When creating a gateway endpoint, you can attach an endpoint policy to it that controls access to the service to which you're connecting.

## Points to Remember for the Exam

- VPC Endpoints allows private connectivity to services hosted in AWS, directly from your VPC without needing an Internet gateway, VPN, Network Address Translation (NAT) devices, or firewall proxies.

- Gateway Endpoints are available for Amazon S3 and DynamoDB.

- Interface Endpoints (powered by AWS PrivateLink) provide private connectivity to many AWS services.

- Endpoints can be used to enforce compliance and security requirements by keeping traffic within the Amazon network, rather than traversing the public internet.

- All traffic between an instance in your VPC and the service does not leave the Amazon network when you use VPC Endpoints.

- You can create an endpoint policy that controls access to the service to which you're connecting. 

- You can also use VPC endpoint policies to control which principal can perform actions, to which resources, and under which conditions.

- When creating a VPC endpoint, you can choose to create an endpoint within a VPC or a VPC endpoint service.

