# AWS Database Migration Service (DMS) Guide

## Overview

AWS Database Migration Service (DMS) helps you migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database.

## Key Features

- **Homogeneous Migrations:** Migrate your databases from one engine to another. For example, Oracle to Oracle.

- **Heterogeneous Migrations:** Migrate from one database engine to another. For example, Microsoft SQL Server to Amazon Aurora.

- **Continuous Data Replication:** Replicate data continuously to support real-time updates to your database.

## Exam Scenarios

1. **Migrating an On-Premises Database to AWS:** DMS can be used to migrate your existing database from on-premises to an AWS-managed database like RDS, Amazon Aurora, or Amazon Redshift. In such scenarios, DMS can handle both homogeneous and heterogeneous migrations.

2. **Database Engine Conversions:** If you're converting from one database engine to another (heterogeneous migration), you might need to use the AWS Schema Conversion Tool (SCT) to convert the source schema and code to match that of the target database.

3. **Minimizing Downtime:** DMS is often used in scenarios where the aim is to minimize downtime. The source database can remain fully operational during the migration, minimizing downtime to applications that rely on it. DMS replicates changes on the source database that occur during the migration process to the target database.

4. **Data Replication Tasks:** In the exam, you might come across scenarios where you need to create data replication tasks. Remember, these tasks can be one-time tasks (migrate existing data and then stop), ongoing tasks (migrate existing data and replicate ongoing changes), or a combination of both.

5. **Multi-AZ:** For critical production level applications, consider using Multi-AZ for the replication instance. If a problem occurs with your primary replication instance, AWS DMS automatically switches to the standby instance.

## Remember

- The source database can be on-premises, on an EC2 instance, or in an RDS database.

- The target database must be on an Amazon EC2 instance or in an RDS database.

- For homogeneous migrations, DMS can typically migrate the database schema for you. For heterogeneous migrations, you might need to use the AWS Schema Conversion Tool (SCT).

- DMS is not just for migration. It can also be used for continuous data replication with high-availability requirements.

## Conclusion

AWS DMS is a powerful tool for migrating and replicating databases. It provides support for widely used databases, offers flexibility in terms of the migration process (one-time or ongoing), and enables you to maintain operational uptime during migrations. Understanding its capabilities and use cases can be vital for the AWS Solutions Architect Associate exam.