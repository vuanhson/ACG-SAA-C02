## Athena vs Macie

### Athena
Interactive query service which enables you to analyse and query data located in S3 using standard SQL
- Serverless, nothing to provision, pay per query / per TB scanned
- No need to set up complex Extract/Transform/Load(ETL) processes
- Works directly with data stored in S3

What Can Athena Be Used For:
- Can be used to query log files stored in S3, e.g. ELB logs, S3 access logs etc
- Generate business reports on data stored in S3
- Analyse AWS cost and usage reports
- Run queries on click-stream data

### Macie
What is PII (Personally Identifiable Information)
- Personal data used to establish an individual’s identity
- This data could be exploited by criminals, used in identity theft and financial fraud
- Home address, email address, SSN
- Passport number, driver’s license number
- D.O.B, phone number, bank account, credit card number

Macie is Security service which uses Machine Learning and NLP (Natural Language Processing) to discover, classify and protect sensitive data stored in S3
- Uses AI to recognise if your S3 objects contain sensitive data such as PII
- Dashboards, reporting and alerts
- Works directly with data stored in S3
- Can also analyze CloudTrail logs
- Great for PCI/DSS and preventing ID theft

### Exam Tips
Remember what Athena is and what it allows you to do:
- Athena is an interactive query service
- It allows you to query data located in S3 using standard SQL
- Serverless
- Commonly used to analyse log data stored in S3

Remember what Macie is and what it allows you to do:
- Macie uses AI to analyze data in S3 and helps identify PII
- Can also be used to analyse CloudTrail logs for suspicious API activity
- Includes Dashboards, Reports and Alerting
- Great for PCI-DSS compliance and preventing ID theft
