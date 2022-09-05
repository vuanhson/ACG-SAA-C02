## Web Application Firewall

Web application firewall that lets you monitor HTTP(S) requests to CloudFront, ALB, or API Gateway
- Control access to content
- Configure filtering rules to allow/deny traffic:
  - IP addresses
  - Query string parameters http://example.com/page?foo=bar&abc=xyz&baz=123
  - SQL query injection
- Blocked traffic returns HTTP 403 Forbidden

WAF allows three different behaviors:
- Allow all requests, except the ones you specify
- Block all requests, except the ones you specify
- Count the requests that match the properties you specify
- Request properties:
  - Originating IP address
  - Originating country
  - Request size
  - Values in request headers
  - Strings in request matching regular expressions (regex) patterns
  - SQL code (injection)
  - Cross-site scripting (XSS

### AWS Firewall Manager
Centrally configure and manage firewall rules across an AWS Organization
- WAF rules:
  - ALB
  - API Gateway
  - CloudFront distributions
- AWS Shield Advanced protections:
  - ALB
  - ELB Classic
  - EIP
  - CloudFront distributions
- Enable security groups for EC2 and ENIs
