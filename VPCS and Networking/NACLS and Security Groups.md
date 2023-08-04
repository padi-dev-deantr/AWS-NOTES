aws # AWS Network ACLs and Security Groups

## Overview

In AWS, both Network Access Control Lists (NACLs) and Security Groups (SGs) play a crucial role in securing your network environment by controlling inbound and outbound traffic.

## Network Access Control Lists (NACLs)

NACLs are a security layer that acts as a firewall for controlling traffic in and out of a VPC subnet. They operate at the subnet level and evaluate traffic entering and leaving subnets.

### Key Characteristics of NACLs

- **Stateless**: This means that NACLs do not maintain context about network connections, and you must specify rules for both inbound and outbound traffic.
  
- **Rule order matters**: Rules are evaluated in order starting from the lowest numbered rule. As soon as a rule matches the traffic, it's applied regardless of any higher-numbered rule that might contradict it.
  
- **Allow/Deny rules**: You can set both ALLOW rules and DENY rules in NACLs.

- **Default NACLs**: Every VPC comes with a default NACL that allows all inbound and outbound IPv4 traffic.
  
- **Custom NACLs**: When you create a custom NACL, by default it denies all inbound and outbound traffic until you add rules.

### Points to Remember for the Exam:

- NACLs can be used to block IP addresses at the subnet level.

- NACLs provide an additional layer of security and can work in conjunction with Security Groups.

## Security Groups

Security Groups are virtual firewalls for your EC2 instances. They control inbound and outbound traffic at the instance level.

### Key Characteristics of Security Groups

- **Stateful**: This means any changes in inbound rules will automatically reflect in outbound rules. If you allow incoming traffic, the outgoing response is automatically allowed, regardless of outbound rules, and vice versa.

- **No DENY rules**: In Security Groups, you can't create explicit deny rules. If you don't explicitly allow traffic, it's automatically denied.

- **Default Security Group**: Every VPC comes with a default Security Group. If you don't specify a different Security Group when you launch an instance, the instance is automatically associated with the default Security Group.

### Points to Remember for the Exam:

- Security Groups operate at the instance level, they support "allow" rules only, and are stateful. 

- If you need to block specific IP addresses, use NACLs, not Security Groups.

- You can associate multiple Security Groups to a single EC2 instance, and a single Security Group can be associated with multiple instances.

Remember that Security Groups and NACLs work together to secure your AWS environment. While NACLs offer a broader level of security for subnets, Security Groups provide more granular control for individual instances. Always consider using both to adhere to the principle of defense in depth.
