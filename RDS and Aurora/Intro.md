## Amazon RDS

Amazon Relational Database Service (RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient, resizable capacity for an industry-standard relational database and manages common database administration tasks.

**Key Features**:

- **Managed Database**: Automates tasks such as hardware provisioning, database setup, patching, and backups.
- **Scalable**: You can scale the compute resources and storage associated with your database instance.
- **Highly Available**: Supports multi-AZ deployments, read replicas, and automated failover.
- **Secure**: Provides several layers of security, including network isolation using Amazon VPC, encryption at rest and in transit, IAM for access control, and more.
- **Compatible**: Supports several database engines such as MySQL, PostgreSQL, MariaDB, Oracle, and SQL Server.

## Amazon RDS Custom

As of my knowledge cutoff in September 2021, there is no specific service called "Amazon RDS Custom". It's possible you might be referring to custom configurations you can apply to your RDS instances, like custom parameter and option groups, custom DB instance classes, etc. These custom configurations allow you to fine-tune your RDS instances to better fit your application's requirements.

## Amazon Aurora

Amazon Aurora is a relational database service that combines the speed and availability of high-end commercial databases with the simplicity and cost-effectiveness of open source databases. It is fully managed by Amazon RDS, which automates time-consuming administration tasks.

**Key Features**:

- **Performance**: Delivers up to five times the throughput of standard MySQL and three times the throughput of standard PostgreSQL.
- **Scalability**: Scales out read traffic across up to 15 Aurora Replicas with minimal impact on write latency.
- **Durability and Availability**: Aurora automatically divides your data into 10GB chunks, and replicates each chunk six times across three Availability Zones.
- **Security**: Provides multiple levels of security for your database, including network isolation using Amazon VPC, encryption at rest and in transit, IAM for access control, and more.
- **Compatible**: Aurora is compatible with MySQL and PostgreSQL, which means code, tools, and applications you use today with your existing databases can be used with Aurora.

These services are designed to take a lot of the administrative heavy-lifting off your hands and allow you to focus on your applications and business logic rather than database management. Your choice between RDS and Aurora will typically depend on your specific use case, budget, and performance needs.