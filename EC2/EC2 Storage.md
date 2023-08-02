

# Amazon EC2 Storage Types

Amazon EC2 supports various types of storage options, which allows it to handle a wide range of workloads. There are primarily three types: EBS, EFS, and Instance Store.

## Amazon [[EBS Storage Types]] (Elastic Block Store)

EBS provides persistent block-level storage volumes for Amazon EC2 instances. An EBS volume behaves like a raw, unformatted, external block device that can be attached to a single instance and are independent of the life of an instance.

- `Pros:`
  - Persistent life span
  - Easily attached or detached from EC2 instances
  - Data can be backed up by taking snapshots
- `Cons:`
  - Can be attached to only one instance at a time
  - It costs more compared to ephemeral storage

## Amazon EFS (Elastic File System)

EFS provides file storage for use with your EC2 instances. It is a network file system that multiple EC2 instances can connect to.

- `Pros:`
  - Multiple EC2 instances can read and write data at the same time
  - Scales automatically as you add or remove files
- `Cons:`
  - Higher latency compared to EBS
  - More expensive compared to EBS and instance store

## Instance Store

Instance Store provides temporary block-level storage for EC2 instances. This storage is located on disks that are physically attached to the host computer.

- `Pros:`
  - Good for buffer and cache for temporary content
  - Provides high I/O and throughput performance
- `Cons:`
  - Not persistent, data will be lost if the instance is stopped or terminated
  - Cannot be resized and you cannot change the volume type

---

These three types of storage options allow you to optimize your storage for your specific needs. EBS is great for many general purposes, EFS is good for scalable file systems, and Instance Store is ideal for temporary storage of information that changes frequently.