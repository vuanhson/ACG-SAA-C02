## High Availability

Everything fails. Everything.

You should always plan for failure.

Scenario: You have a website that requires a minimum of 6 instances and it must be highly available. You must also be able to tolerate the failure of 1 Availability Zone. What is the ideal architecture for this environment while also being the most cost effective?
- 2 Availability Zones with 2 instances in each AZ.
- **3 Availability Zones with 3 instances in each AZ.**
- 1 Availability Zone with 6 instances in each AZ.
- 3 Availability Zones with 2 instances in each AZ.

Remember the following
- Always Design for failure.
- Use Multiple AZ’s and Multiple Regions where ever you can.
- Know the difference between Multi-AZ and Read Replicas for RDS.
- Know the difference between scaling out and scaling up.
- Read the question carefully and always consider the cost element.
- Know the different S3 storage classes.
