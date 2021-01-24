## Cloudwatch 101

### Cloudwatch
Amazon Cloudwatch is a monitoring service to monitor your AWS resources, as well as the applications that you run on AWS

What Can I do With CloudWatch
- Dashboards - Creates awesome dashboards to see what is happening with your AWS environment.
- Alarms - Allows you to set Alarms that notify you when particular thresholds are hit.
- Events - CloudWatch Events helps you to respond to state changes in your AWS resources.
- Logs - CloudWatch Logs helps you to aggregate, monitor, and store logs.

Cloudwatch can monitor things like
- Compute:
  - EC2 Instances
  - Autoscaling Groups
  - Elastic Load Balancer
  - Route53 Health Checks
- Storage
  - EBS Volume
  - Storage Gateways
  - CloudFront

etc...

Host level metrics consist of:
- CPU
- Network
- Disk
- Status Check

### Cloudtrail
AWS Cloudtrail increases visibility into your user and resource activity by recording AWS Management Console actions and API calls. You can identify which users and accounts called AWS, the source IP address from which the calls were made, and when the calls occured.

### Exam Tips
- Cloudwatch is used for monitoring performance
- Cloudwatch can monitor most of AWS as well as your applications that run on AWS
- Cloudwatch with EC2 will monitor events every 5 minutes by default (Standard monitoring)
- You can have 1 minute intervals by turning on detailed monitoring (Detailed monitoring)
- You can create Cloudwatch alarms which trigger notifications
- Cloudwatch is all about performance. CloudTrail is all about auditing
- What Can I do With CloudWatch (see above)
- CloudWatch monitors performance. CloudTrail monitors API calls in the AWS platform.
