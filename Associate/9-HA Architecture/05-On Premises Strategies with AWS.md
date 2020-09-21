## On-Premises strategies with AWS

You need to be aware of what high-level AWS services you can use on-premises for the exam:
- Database Migration Service (DMS): See Section 5, chap 08
- Server Migration Service (SMS)
  - Server Migration Service supports incremental replication of your on-premises servers in to AWS.
  - Can be used as a backup tool, multi-site strategy (on-premises and off-premises), and a DR tool.
- AWS Application Discovery Service
  - AWS Application Discovery Service helps enterprise customers plan migration projects by gathering information about their on-premises data centers.
  - You install the AWS Application Discovery Agentless Connector as a virtual appliance on VMware vCenter.
  - It will then build a server utilization map and dependency map of your on-premises environment.
  - The collected data is retained in encrypted format in an AWS Application Discovery Service data store. You can export this data as a CSV file and use it to estimate the Total Cost of Ownership (TCO) of running on AWS and to plan your migration to AWS.
  - This data is also available in AWS Migration Hub, where you can migrate the discovered servers and track their progress as they get migrated to AWS.
- VM Import/Export
  - Migrate existing applications in to EC2.
  - Can be used to create a DR strategy on AWS or use AWS as a second site.
  - You can also use it to export your AWS VMs to your on-premises data center.
- Download Amazon Linux 2 as an ISO
  - AWS allows you to download Amazon Linux 2 as an ISO
  - Works with all major virtualization providers, such as VMware, Hyper-V, KVM, VirtualBox (Oracle), etc.
