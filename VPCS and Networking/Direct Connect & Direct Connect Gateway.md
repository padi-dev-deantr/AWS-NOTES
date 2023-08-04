# AWS Direct Connect and Direct Connect Gateway

AWS Direct Connect is a service that establishes a dedicated, private network connection from your on-premises network to AWS. Direct Connect Gateway is a globally available resource that helps you manage your Direct Connect connections across multiple AWS Regions and VPCs.

## Basic Concepts

- **AWS Direct Connect:** A service that provides dedicated, private connectivity between your datacenter, office, or colocation environment and AWS.

- **Direct Connect Gateway:** A globally available resource that you can use to manage your Direct Connect connections. You can associate multiple VPCs from different AWS Regions with your Direct Connect gateway.

## Creating a Direct Connect Connection

Here are the basic steps to set up a Direct Connect connection:

1. **Request a Direct Connect Connection:** In the AWS Management Console, navigate to Direct Connect > Connections > Create Connection. Select your location and port speed.

2. **Set up your connection:** After your request is accepted, you (or your network provider) need to establish a cross-connect at the chosen Direct Connect location.

3. **Create a Direct Connect Gateway:** In the AWS Management Console, navigate to Direct Connect > Direct Connect Gateways > Create Direct Connect Gateway. 

4. **Create a Virtual Interface:** You need to create a Virtual Interface to enable connectivity between your Direct Connect connection and your VPC.

## Exam Tips

- AWS Direct Connect provides a more consistent network experience than Internet-based connections.

- Direct Connect Gateway allows you to connect to multiple VPCs across different AWS Regions.

- Direct Connect supports two types of virtual interfaces: private (to access your VPC) and public (to access public AWS services).

- With Direct Connect, data transferred out of AWS is billed at the reduced Direct Connect data transfer rate rather than Internet data transfer rates.

- AWS Direct Connect is compatible with all AWS services. It's not a service-to-service connection, but a network service.

- Direct Connect connections are always made to a specific Direct Connect location, and each connection is always associated with a single AWS account.

- Each Direct Connect connection can be partitioned into multiple virtual interfaces, allowing the same connection to be used to access public resources and VPC resources while maintaining network separation between the environments. 

Example code to create a Direct Connect Gateway:

```bash
aws directconnect create-direct-connect-gateway --direct-connect-gateway-name MyDCGateway --amazon-side-asn 65000
```

Example code to create a Direct Connect connection:

```bash
aws directconnect create-connection --location DXLocation --bandwidth 1Gbps --connection-name MyDXConnection
```

Replace `DXLocation`, `1Gbps`, and `MyDXConnection` with your desired Direct Connect location, bandwidth, and connection name, respectively.