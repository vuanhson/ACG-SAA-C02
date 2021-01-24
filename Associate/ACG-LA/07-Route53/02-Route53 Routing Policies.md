## Route53 Routing Policies Available On AWS
The Following Routing Policies Are Available With Route53:
- Simple Routing
- Weighted Routing
- Latency-based Routing
- Failover Routing
- Geolocation Routing
- Geoproximity Routing (Traffic Flow Only)
- Multivalue Answer Routing

### Simple Routing Policy
If you choose the simple routing policy you can only have one record with multiple IP addresses. If you specify multiple values in a record, Route 53 returns all values to the user in a random order.

### Weighted Routing Policy
- Allows you split your traffic based on different weights assigned.
- For example, you can set 10% of your traffic to go to US-EAST-1 and 90% to go to EU-WEST-1.
- Health Checks:
  - You can set health checks on individual record sets.
  - If a record set fails a health check it will be removed from Route53 until it passes the health check.
  - You can set SNS notifications to alert you if a health check is failed.

### Latency-Based Policy
Allows you to route your traffic based on the lowest network latency for your end user (ie which region will give them the fastest response time).

To use latency-based routing, you create a latency resource record set for the Amazon EC2 (or ELB) resource in each region that hosts your website. When Amazon Route 53 receives a query for your site, it selects the latency resource record set for the region that gives the user the lowest latency. Route 53 then responds with the value associated with that resource record set.

### Geolocation Routing Policy
Geolocation routing lets you choose where your traffic will be sent based on the geographic location of your users (ie the location from which DNS queries originate). For example, you might want all queries from Europe to be routed to a fleet of EC2 instances that are specifically configured for your European customers. These servers may have the local language of your European customers and all prices are displayed in Euros.

### Failover Routing Policy
- Failover routing policies are used when you want to create an active/passive set up. For example, you may want your primary site to be in EU-WEST-2 and your secondary DR Site in AP-SOUTHEAST-2. 
- Route53 will monitor the health of your primary site using a health check. 
- A health check monitors the health of your end points

### Geoproximity Routing (Traffic Flow Only)
Geoproximity routing lets Amazon Route 53 route traffic to your resources based on the geographic location of your users and your resources. You can also optionally choose to route more traffic or less to a given resource by specifying a value, known as a bias. A bias expands or shrinks the size of the geographic region from which traffic is routed to a resource. 

To use geoproximity routing, you must use Route 53 traffic flow.

### Multivalue Answer Policy
Multivalue answer routing lets you configure Amazon Route 53 to return multiple values, such as IP addresses for your web servers, in response to DNS queries. You can specify multiple values for almost any record, but multivalue answer routing also lets you check the health of each resource, so Route 53 returns only values for healthy resources.

This is similar to simple routing however it allows you to put health checks on each record set.