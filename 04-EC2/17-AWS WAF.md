## AWS WAF

AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to Amazon CloudFront, an Application Load Balancer or API Gateway. AWS WAF also lets you control access to your content.

You can configure conditions such as what IP addresses are allowed to make this request or what query string parameters need to be passed for the request to be allowed. Then the application load balancer or CloudFront or API Gateway will either allow this content to be received or to give a HTTP 403 Status Code.

At its most basic level, AWS WAF allows 3 different behaviours:
- Allow all requests except the ones you specify
- Block all requests except the ones you specify
- Count the requests that match the properties you specify

Extra protection against web attacks using conditions you specify. You can define conditions by using characteristics of web requests such as:
- IP addresses that requests originate from.
- Country that requests originate from.
- Values in request headers.
- Strings that appear in requests, either specific strings or string that match regular expression (regex) patterns.
- Length of requests.
- Presence of SQL code that is likely to be malicious (known as SQL injection).
- Presence of a script that is likely to be malicious (known as cross-site scripting).

### Exam Tips
In the exam you will be given different scenarios and you will be asked how to block malicious IP addresses
- Use AWS WAF
- Use Network ACLs - We will cover this in more detail in the VPC section
