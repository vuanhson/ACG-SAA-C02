## S3 Security and Encryption

### The Basics
- By default, all newly created buckets are PRIVATE. You can setup access control to your buckets using:
  - Bucket Policies (Bucket level)
  - Access Control Lists (Individual object level)
- S3 buckets can be configured to create access logs which log all requests made to the S3 bucket. This can be sent to another bucket and even another bucket in another account.
- Encryption In Transit is achieved by:
  - SSL/TLS
- Encryption At Rest (Server Side) is achieved by
  - S3 Managed Keys - SSE-S3
  - AWS Key Management Service, Managed Keys - SSE-KMS
  - Server Side Encryption With Customer Provided Keys - SSE-C
- Client Side Encryption