# Classless Inter-Domain Routing (CIDR)

Classless Inter-Domain Routing (CIDR) is a method used to allocate IP addresses and route them. It replaced the older system known as Classful networking to provide more efficient use of IP address space. CIDR allows for close control of IP address allocations, and thus, more efficient use of allocations.

## CIDR Notation

CIDR notation is a standard syntax for writing IPv4 and IPv6 addresses along with their associated routing prefix. It consists of an IP address, a slash ('/') character, and a decimal number. The IP address represents the network address, and the decimal number, known as the prefix length, indicates how many high-order bits of the address comprise the network address. For example, in CIDR notation `192.0.2.0/24`, `192.0.2.0` is the network address and `24` is the prefix length, which is the number of bits that make up the network address.

## CIDR Blocks

A CIDR block is an IP address range defined by a network address and a CIDR prefix. AWS uses CIDR blocks to specify network addresses for VPCs and subnets. A VPC CIDR block is the range of valid IP addresses available for assignment within the VPC. A subnet CIDR block is a subset of the VPC CIDR block assigned to a subnet within the VPC.

## Important Points

- The smallest CIDR block you can allocate is `/28` and the largest is `/16`.
- The number of IP addresses in a subnet defined by a CIDR block is `2^(32 - block size)` - 2. The "-2" reserves an address for network routing and the broadcast address. For example, a `/24` CIDR block gives you `2^(32-24) - 2 = 254` usable addresses.
- In AWS, a VPC can have one IPv4 CIDR block and multiple associated IPv6 CIDR blocks.
- For subnetting, AWS reserves the first four IP addresses and the last IP address in each subnet CIDR block. They're not available for you to use.

Example:
If you have a CIDR block `10.0.0.0/16` for your VPC, you can create multiple subnets within this block. For example, a `10.0.1.0/24` subnet and a `10.0.2.0/24` subnet.

## Exam Tips

- In AWS, you cannot overlap CIDR blocks. So, when you're setting up peering relationships or configuring your VPC, ensure your CIDR blocks do not overlap.
- Understanding CIDR notation and how to calculate available addresses in a block is crucial for the exam.

>[!info]
>In Amazon VPC, AWS reserves five (5) IP addresses within each subnet CIDR block.
These reserved IP addresses are: 
> - The first four and the last IP address in each subnet CIDR block are not available for you to use and cannot be assigned to an instance.
> For example, in a subnet with CIDR block 10.0.0.0/24, the following IP addresses are reserved: 
> - 10.0.0.0: Network address.
> - 10.0.0.1: Reserved by AWS for the VPC router.
> - 10.0.0.2: Reserved by AWS for Amazon-provided DNS.
> - 10.0.0.3: Reserved by AWS for future use.
> - 10.0.0.255: Network broadcast address. AWS does not support broadcast in a VPC, therefore, they reserve this address.
> 
Please note, if you need to determine the number of available IP addresses within a subnet, subtract 5 from the total number of IP addresses for the subnet's CIDR block. For example, with a /24 CIDR block, there are 256 total IP addresses, so you would have 251 available for your instances.