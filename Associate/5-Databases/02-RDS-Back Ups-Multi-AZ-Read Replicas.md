## RDS - Back Ups, Multi-AZ & Read Replicas

There are two different types of Backups for RDS:
- Automated Backups
- Database Snapshots

### Automated Backups
Automated Backups allow you to recover your database to any point in time within a “retention period”. The retention period can be between one and 35 days. Automated Backups will take a full daily snapshot and will also store transaction logs throughout the day. When you do a recovery, AWS will first choose the most recent daily back up, and then apply transaction logs relevant to that day. This allows you to do a point in time recovery down to a second, within the retention period.

Automated Backups are enabled by default. The backup data is stored in S3 and you get free storage space equal to the size of your database. So if you have an RDS instance of 10Gb, you will get 10Gb worth of storage.

Backups are taken within a defined window. During the backup window, storage I/O may be suspended while your data is being backed up and you may experience elevated latency.

### Database Snapshots
DB Snapshots are done manually (ie they are user initiated.) They are stored even after you delete the original RDS instance, unlike automated backups.

### Restoring Backups
Whenever you restore either an Automatic Backup or a manual Snapshot, the restored version of the database will be a new RDS instance with a new DNS endpoint.

### Encryption At Rest
Encryption at rest is supported for MySQL, Oracle, SQL Server, PostgreSQL, MariaDB & Aurora. Encryption is done using the AWS Key Management Service (KMS) service. Once your RDS instance is encrypted, the data stored at rest in the underlying storage is encrypted, as are its automated backups, read replicas, and snapshots.

### What is Multi-AZ
Multi-AZ allows you to have an exact copy of your production database in another Availability Zone. AWS handles the replication for you, so when your production database is written to, this write will automatically be synchronized to the stand by database.

In the event of planned database maintenance, DB Instance failure, or an Availability Zone failure, Amazon RDS will automatically failover to the standby so that database operations can resume quickly without administrative intervention.

Multi-AZ is for Disaster Recovery only, It is not primarily used for improving performance. For performance improvement, you need Read Replicas. You can force a failover from one AZ to another by rebooting the RDS instance.

Multi-AZ is available for the following databases: SQL Server, Oracle, MySQL Server, PostgreSQL, MariaDB

### What is Read Replica
Read replicas allow you to have a read-only copy of your production database. This is achieved by using Asynchronous replication from the primary RDS instance to the read replica. You use read replicas primarily for very read-heavy database workloads.

Read Replicas are available for the following databases: MySQL Server, PostgreSQL,  MariaDB, Oracle, Aurora, MSSQL

Things to know about Read Replicas:
- Used for scaling, not for DR!
- Must have automatic backups turned on in order to deploy a read replica.
- You can have up to 5 read replica copies of any database. (15 with Aurora)
- You can have read replicas of read replicas (but watch out for latency.)
- Each read replica will have its own DNS endpoint.
- You can have read replicas that have Multi-AZ.
- You can create read replicas of Multi-AZ source databases.
- Read replicas can be promoted to be their own databases. This breaks the replication.
- You can have a read replica in a second region.