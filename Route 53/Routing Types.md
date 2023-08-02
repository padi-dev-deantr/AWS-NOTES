## 1. Simple Routing

This is the default routing policy when you create a new record set. This is most commonly used when you have a single resource that performs a given function for your domain, like one web server that hosts your website.

## 2. Weighted Routing

Weighted routing lets you split your traffic based on different weights assigned. For example, you might want 60% of your traffic to go to your primary server and 40% to go to a backup server.

## 3. Latency-based Routing

This type of routing is used when you have resources in multiple AWS Regions and you want to route traffic to the region that provides the best latency. When a user queries the DNS for your site, Amazon Route 53 selects the latency resource record for the region that gives the user the lowest latency.

## 4. Failover Routing

This policy is used when you want to create an active-passive setup. For example, you might want your primary web server to serve all traffic, but if it goes down, you want a secondary backup web server to take all the traffic.

## 5. Geolocation Routing

Geolocation routing lets you choose where your traffic will be sent based on the geographic location of your users.

## 6. Geoproximity Routing (Traffic Flow Only)

This policy lets you route traffic based on the geographic location of your users and your resources. You can also optionally choose to route more traffic or less to a given resource by specifying a bias.

## 7. Multivalue Answer Routing

Multivalue answer routing lets you return multiple values, such as IP addresses for your web servers, in response to DNS queries. You can also associate Amazon Route 53 health checks with the records so Route 53 will not return a value for a record when the health check is failing.

Remember, to change routing policies, you update the records in your hosted zone. These changes take effect typically within 60 seconds. The choice of routing policy largely depends on your use case and configuration of your resources. Be sure to test your configuration to make sure it behaves as expected.
