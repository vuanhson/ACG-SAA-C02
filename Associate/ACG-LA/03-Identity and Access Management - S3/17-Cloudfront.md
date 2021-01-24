## Cloudfront

### What is CloudFront?
A content delivery network (CDN) is a system of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage, and a content delivery server.

Amazon CloudFront can be used to deliver your entire website, including dynamic, static, streaming, and interactive content using a global network of edge locations. Requests for your content are automatically routed to the nearest edge location, so content is delivered with the best possible performance.
### Key Terminology
- Edge Location - This is the location where content will be cached. This is separate to an AWS Region/AZ.
- Origin - This is the origin of all the files that the CDN will distribute. This can be an S3 Bucket, an EC2 Instance, an Elastic Load Balancer, or Route53.
- Distribution - This is the name given the CDN which consists of a collection of Edge Locations.
- Web Distribution - Typically used for Websites.
- RTMP - Used for Media Streaming.

### Other notes: 
- Edge locations are not just READ only — you can write to them too. (ie put an object on to them.)
- Objects are cached for the life of the TTL (Time To Live.)
- You can invalidate cached objects, but you will be charged.