## Elastic Load Balancer

- Application Load Balancers are best suited for load balancing of HTTP and HTTPS traffic. They operate at Layer 7 and are applicationaware. They are intelligent, and you can create advanced request routing, sending specified requests to specific web servers.

- Network Load Balancers are best suited for load balancing of TCP traffic where extreme performance is required. Operating at the connection level (Layer 4), Network Load Balancer are capable of handling millions of requests per second,while maintaining ultra-low latencies. Use for extreme performance!

- Classic Load Balancers are the legacy Elastic Load Balancers. You can load balance HTTP/HTTPS applications and use Layer 7-specific features, such as X-Forwarded and sticky sessions. You can also use strict Layer 4 load balancing for applications that rely purely on the TCP protocol.

### Errors in Load Balancing
Classic Load Balancers - if your application stops responding, the ELB (Classic Load Balancer) responds with a 504 (Gateway Time out) error. This means that the application is having issues. This could be either at the Web Server layer or at the Database Layer. Identify where the application is failing, and scale it up or out where possible.

### What Are Sticky Sessions?
- Sticky sessions allow you to bind a user's session to a specific EC2 instance. This ensures that all requests from the user during the session are sent to the same instance.
- You can enable Sticky Sessions for Application Load Balancers as well, but the traffic will be sent at the Target Group Level.
- Can be useful if you are storing information locally to that instance.

### Cross Zone Load Balancing
The nodes for your load balancer distribute requests from clients to registered targets. When cross-zone load balancing is enabled, each load balancer node distributes traffic across the registered targets in all enabled Availability Zones.

https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/how-elastic-load-balancing-works.html

### Path Patterns
You can create a listener with rules to forward requests based on the URL path. This is known as path-based routing. If you are running microservices, you can route traffic to multiple back-end services using path-based routing. For example, you can route general requests to one target group and requests to render images to another target group.

### Exam Tips
- If you need the IPv4 address of your end user, look for the X-Forwarded-For header.
- Instances monitored by Classic LB are reported as InService or OutofService
- Health Checks check the instance health by talking to it.
- Load Balances have their own DNS name. You are never given an IP address.
