**Overview**: EC2 allows users to rent virtual computers on which to run their own computer applications. It's designed to make web-scale cloud computing easier for developers. You can create an instance (a virtual server) in the AWS cloud, configure the security and networking, and manage storage.

```bash
# Launch an instance
aws ec2 run-instances --image-id ami-abc12345 --count 1 --instance-type t2.micro --key-name MyKeyPair --security-group-ids sg-903004f8 --subnet-id subnet-6e7f829e
```

**Use Cases**: EC2 is used in a variety of applications such as:

- Web & Application Hosting: By replacing traditional server hosting with EC2, you can significantly improve scalability and availability.
- Big Data Analytics: Utilize EC2's computational power to analyze vast amounts of data.
- Gaming: Power your backend servers for online gaming experiences.
- High-Performance Computing: Deploy high-performance applications in fields like genomics, finance, simulation, etc.

**Instance Types**: Amazon EC2 provides a variety of instance types optimized to fit different use cases. They come in various hardware configurations and cater to compute, memory, storage, and GPU needs. 

```bash
# List instance types details
aws ec2 describe-instance-types --query "InstanceTypes[?InstanceType=='m5.xlarge']"
```

**Security Groups**: A security group acts as a virtual firewall for your instance to control inbound and outbound traffic. You add rules to each security group to allow traffic to and from its associated instances. 

```bash
# Create a security group
aws ec2 create-security-group --group-name my-sg --description "My security group"
```

**Elastic IP Addresses**: An Elastic IP address is a static, public IPv4 address designed for dynamic cloud computing. An Elastic IP address is associated with your AWS account, and they allow you to mask the failure of an instance by remapping your public IP addresses to another instance in your account.

```bash
# Allocate an Elastic IP address
aws ec2 allocate-address
```

**AMI (Amazon Machine Images)**: AMIs are templates that contain the software configuration (operating system, application server, and applications) required to launch your instance. You can select an AMI provided by AWS, user community, or through the AWS Marketplace. You can also create your own AMIs.

```bash
# Create an AMI from an instance
aws ec2 create-image --instance-id i-1234567890abcdef0 --name "My server"
```

**Auto Scaling**: Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. 

```bash
# Create an Auto Scaling group
aws autoscaling create-auto-scaling-group --auto-scaling-group-name my-asg --launch-configuration-name my-launch-config --min-size 1 --max-size 5 --vpc-zone-identifier "subnet-0ff156e0c4a6d3001"
```

**Storage**: EC2 supports multiple storage options (EBS, EFS, and instance store) each designed for specific workloads. 

**Key Pairs**: Amazon EC2 uses public–key cryptography to encrypt and decrypt login information. To log in to your instance, you must create a key pair, specify the name of the key pair when you launch the instance, and provide the private key when you connect to the instance.

```bash
# Create a key pair
aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem
```

**Spot Instances**: Spot Instances are spare EC2 instances available at up to a 90% discount compared to On-Demand prices. You can use Spot Instances for various stateless, fault-tolerant, or flexible applications.

```bash
# Request Spot Instances
aws ec2 request-spot-instances --spot-price "0.05" --instance-count 1 --type "one-time" --launch-specification file://my-spot-instance.json
```

These are just the basics of Amazon EC2. The EC2 service has many more features and capabilities that allow for a flexible, secure, and powerful cloud computing platform.