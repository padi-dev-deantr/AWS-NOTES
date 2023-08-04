# AWS Transit Gateway

AWS Transit Gateway is a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and on-premises networks to a single gateway. 

## Basic Concepts

- **Transit Gateway:** This is a network transit hub that you can use to interconnect your VPCs and on-premises networks.

- **Transit Gateway Attachments:** These are the connections from a VPC or VPN connection to a transit gateway.

- **Transit Gateway Route Tables:** They are used to determine where network traffic is directed. Each transit gateway starts with a default route table.

## Creating a Transit Gateway

Here are the basic steps to set up a Transit Gateway:

1. **Create a Transit Gateway:** Navigate to VPC > Transit Gateways > Create Transit Gateway. Provide the required information and create the gateway.

2. **Create Transit Gateway Attachments:** You need to create attachments for each VPC or VPN connection that needs to connect to the transit gateway.

3. **Modify Route Tables:** In your VPC, you'll need to modify your route tables to direct traffic to the transit gateway.

## Exam Tips

- AWS Transit Gateway acts as a hub that controls how traffic is routed among all the connected networks which act like spokes.

- Transit Gateway simplifies management and reduces operational costs because you don’t need to maintain individual peering connections between your networks.

- With Transit Gateway, you can apply routing and security policies in a central location, which enhances your network architecture and overall security posture.

- AWS Transit Gateway supports VPN and Direct Connect attachments, allowing you to centralize and streamline your connectivity to the AWS cloud.

Example code to create a Transit Gateway:

```bash
aws ec2 create-transit-gateway --description "my transit gateway"
```

Example code to attach a VPC to a Transit Gateway:

```bash
aws ec2 create-transit-gateway-vpc-attachment --transit-gateway-id tgw-0abc123def456ghij --vpc-id vpc-01abc23d4efgh5678 --subnet-ids subnet-a1b2c3d4 subnet-e5f6g7h8
```

