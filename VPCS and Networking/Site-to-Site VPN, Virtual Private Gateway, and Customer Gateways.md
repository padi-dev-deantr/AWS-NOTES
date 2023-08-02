# Site-to-Site VPN, Virtual Private Gateway, and Customer Gateways

Site-to-Site VPN, Virtual Private Gateway, and Customer Gateways are key components of the AWS VPN service, which enables secure communication between your on-premises networks and your Amazon Virtual Private Cloud (VPC).

## Basic Concepts

- **Site-to-Site VPN:** This is a secure connection between your on-premises network and your VPCs.

- **Virtual Private Gateway (VGW):** This is the VPN concentrator on the AWS side of the Site-to-Site VPN connection. It's a logical entity associated with your VPC.

- **Customer Gateway (CGW):** This is a resource that you create in AWS that represents the customer gateway device in your on-premises network.

## Creating a Site-to-Site VPN Connection

Here are the basic steps to set up a Site-to-Site VPN connection:

1. **Create a Customer Gateway (CGW)**: In the AWS Management Console, navigate to VPC Dashboard > Customer Gateways > Create Customer Gateway. You need to specify the public IP address of your on-premises VPN device.

2. **Create a Virtual Private Gateway (VGW)**: In the AWS Management Console, navigate to VPC Dashboard > Virtual Private Gateways > Create Virtual Private Gateway. You need to attach this VGW to the desired VPC.

3. **Create a Site-to-Site VPN connection**: In the AWS Management Console, navigate to VPC Dashboard > Site-to-Site VPN Connections > Create VPN Connection. You need to specify the VGW and CGW to create this connection.

4. **Configure your Customer Gateway**: You will get configuration information from AWS once the Site-to-Site VPN connection is created. You need to apply this configuration on your on-premises VPN device.

## Exam Tips

- Each VPN connection consists of two VPN tunnels, which you can simultaneously use for high availability.

- AWS uses the Border Gateway Protocol (BGP) for dynamic routing with your on-premises network. You need to specify BGP Autonomous System Number (ASN) when you create the CGW.

- You can monitor your Site-to-Site VPN connections using Amazon CloudWatch, which can report metrics such as bytes transferred and number of packets.

- AWS VPN is a managed service, which means AWS will automatically manage the availability and scalability of the VPN endpoints.