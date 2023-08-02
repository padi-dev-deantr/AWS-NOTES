# AWS VPC Peering

## Overview

Amazon Virtual Private Cloud (VPC) Peering allows you to connect one VPC with another via a direct network route using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they were within the same network.

## Key Characteristics of VPC Peering

- **Inter-region VPC Peering**: Allows peering between VPCs across different AWS regions. This can help to reduce latency in your applications by providing a direct network route between VPCs in different regions.

- **Transitive Peering**: AWS does not support transitive peering relationships. This means if VPC A is peered with VPC B, and VPC B is peered with VPC C, VPC A and VPC C are not implicitly peered. Each peering connection is a one-to-one relationship.

- **Overlapping CIDR Blocks**: VPCs with overlapping CIDR blocks cannot be peered. It's important to plan your CIDR ranges in advance to ensure that there's no overlap if you want to establish a peering connection.

- **No Single Points of Failure**: VPC Peering connections do not rely on a single physical connection, and thus are not susceptible to connectivity issues from a single point of failure.

- **Traffic Restrictions**: VPC Peering traffic does not traverse the public internet, thus reducing exposure to threat vectors such as malicious attacks.

## Points to Remember for the Exam:

- VPC Peering is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 or IPv6 addresses. 

- AWS uses existing infrastructure to create a VPC Peering connection. It is neither a gateway nor a VPN connection, and it does not rely on a separate piece of physical hardware. 

- There is no single point of failure for communication or a bandwidth bottleneck.

- VPC Peering connection can be created between your own VPCs, or with a VPC in another AWS account within a single region (Intra-Region VPC Peering) or between regions (Inter-Region VPC Peering).

- VPCs across different AWS Organizations can also be peered together.

- VPC Peering does not support transitive routing. For instance, if VPC A is peered with VPC B, and VPC B is peered with VPC C, there isn't automatic connectivity between VPC A and VPC C.