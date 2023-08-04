# AWS VPC Traffic Mirroring

AWS VPC Traffic Mirroring is a feature that allows you to capture and inspect network traffic in your Virtual Private Cloud (VPC). 

## Basic Concepts

- **Traffic Mirroring:** This is the action of duplicating network traffic from an EC2 instance and directing it to another instance for analysis.

- **Traffic Mirror Source:** This is the source of the network traffic. It can be an EC2 instance or a network interface.

- **Traffic Mirror Target:** This is the destination for the mirrored traffic. It can be a network interface or a Network Load Balancer.

- **Traffic Mirror Filter:** This determines the type of traffic to mirror. You can choose to mirror all traffic or just a subset.

- **Traffic Mirror Session:** This binds a mirror source to a mirror target and applies a traffic mirror filter.

## How to Set Up VPC Traffic Mirroring

Here are the basic steps to set up VPC Traffic Mirroring:

1. **Create a Traffic Mirror Target:** This could be a network interface or a Network Load Balancer.

2. **Create a Traffic Mirror Filter:** This will determine what traffic gets mirrored.

3. **Create a Traffic Mirror Session:** This binds the Mirror Source (the instance you want to mirror traffic from) to the Mirror Target and applies the Traffic Mirror Filter.

4. **Analyze the Mirrored Traffic:** The mirrored traffic can be analyzed by running tools such as IDS/IPS, monitoring, or troubleshooting tools on the instance that's associated with the mirror target.

## Exam Tips

- VPC Traffic Mirroring is available with EC2 instances, providing the ability to capture and inspect network traffic in your VPC.

- The Traffic Mirroring feature helps with content inspection, threat monitoring, and troubleshooting.

- Traffic Mirroring supports filters so that you only mirror the traffic of interest. You can filter by traffic direction, protocol, source and destination CIDR blocks, and source and destination ports.

- VPC Traffic Mirroring is only available for instances running in a Virtual Private Cloud (VPC). It does not support instances running on the EC2-Classic platform.

Example code to create a Traffic Mirror Target:

```bash
aws ec2 create-traffic-mirror-target --network-interface-id eni-xyz --description "Traffic mirror target for instance XYZ"
```

Example code to create a Traffic Mirror Filter and a rule:

```bash
aws ec2 create-traffic-mirror-filter --description "My traffic mirror filter"
aws ec2 create-traffic-mirror-filter-rule --traffic-mirror-filter-id tmf-abc --traffic-direction ingress --rule-action accept --protocol 6 --source-cidr-block 0.0.0.0/0 --destination-cidr-block 0.0.0.0/0 --rule-number 1 --description "Ingress filter rule"
```

Replace `eni-xyz`, `tmf-abc`, and other placeholder values with actual IDs.