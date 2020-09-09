## EC2 Placement Groups

### Three Types of Placement Groups
- Clustered Placement Group
- Spread Placement Group
- Partitioned

### Clustered Placement Group
A cluster placement group is a grouping of instances within a single Availability Zone. Placement groups are recommended for applications that need low network latency, high network throughput, or both.

Only certain instances can be launched in to a Clustered Placement Group.

### Spread Placement Group
A spread placement group is a group of instances that are each placed on distinct underlying hardware.

Spread placement groups are recommended for applications that have a small number of critical instances that should be kept separate from each other.

### Partitioned Placement Group
When using partition placement groups, Amazon EC2 divides each group into logical segments called partitions. Amazon EC2 ensures that each partition within a placement group has its own set of racks. Each rack has its own network and power source. No two partitions within a placement group share the same racks, allowing you to isolate the impact of hardware failure within your application.

### Notes
- Clustered Placement Group: Low Network Latency / High Network Throughput
- Spread Placement Group: Individual Critical EC2 instances
- Partitioned: Multiple EC2 instances HDFS, HBase, and Cassandra

### Exam Tips
- A clustered placement group can't span multiple Availability Zones.
- A spread placement and partitioned group can.
- The name you specify for a placement group must be unique within your AWS account.
- Only certain types of instances can be launched in a placement group (Compute Optimized, GPU, Memory Optimized, Storage Optimized)
- AWS recommend homogenous instances within clustered placement groups.
- You can't merge placement groups.
- You can move an existing instance into a placement group. Before you move the instance, the instance must be in the stopped state. You can move or remove an instance using the AWS CLI or an AWS SDK, you can’t do it via the console yet.
