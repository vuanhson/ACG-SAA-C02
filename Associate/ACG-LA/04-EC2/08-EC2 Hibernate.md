## EC2 Hibernate

We have learned so far we can stop and terminate EC2 instances. If we stop the instance, the data is kept on the disk (with EBS) and will remain on the disk until the EC2 instance is started. If the instance is terminated, then by default the root device volume will also be terminated.

When we start our EC2 instance, the following happens:
- Operating system boots up
- User data script is run (bootstrap scripts)
- Applications start (can take some time)

When you hibernate an EC2 instance, the operating system is told to perform hibernation (suspend-to-disk). Hibernation saves the contents from the instance memory (RAM) to your Amazon EBS root volume. We persist the instance’s Amazon EBS root volume and any attached Amazon EBS data volumes.

When you start your instance out of hibernation:
- The Amazon EBS root volume is restored to its previous state
- The RAM contents are reloaded
- The processes that were previously running on the instance are resumed
- Previously attached data volumes are reattached and the instance retains its instance ID

With EC2 Hibernate, the instance boots much faster. The operating system does not need to reboot because the in-memory state (RAM) is preserved. This is useful for:
- Long-running processes
- Services that take time to initialize

### Exam Tips:
- EC2 Hibernate preserves the in-memory RAM on persistent storage (EBS)
- Much faster to boot up because you do not need to reload the operating system
- Instance RAM must be less than 150 GB
- Instance families include C3, C4, C5, M3, M4, M5, R3, R4, and R5
- Available for Windows, Amazon Linux 2 AMI, and Ubuntu
- Instances can’t be hibernated for more than 60 days
- Available for On-Demand instances and Reserved Instances