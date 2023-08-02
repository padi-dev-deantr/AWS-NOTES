## Application Load Balancer (ALB)

The Application Load Balancer is a type of Elastic Load Balancer that operates at the application layer or Layer 7 of the OSI model. It is designed to handle HTTP and HTTPS traffic and provides advanced routing features compared to the classic Elastic Load Balancer.

### Features of ALB

- **Content-Based Routing**: ALB allows you to route traffic based on the content of the HTTP(S) request. You can define rules to route requests to different targets based on the URL, hostname, HTTP headers, methods, and fields in the request.

- **Host and Path-Based Routing**: This allows you to route requests based on the host field of the HTTP header (for example, to route requests to different domains to different backend services) and on the URL path (for example, `/images/*` could go to an image-processing backend, and `/api/*` could go to your API servers).

- **Support for Container-Based Applications**: With ALB, you can register targets in a target group using their IP addresses, which is particularly useful for container-based applications.

- **Built-In Metrics and Request Tracing**: ALB provides several CloudWatch metrics, and also access logs that provide detailed records of requests.

- **Support for WebSocket and HTTP/2 Protocols**: ALB provides native support for WebSocket and HTTP/2 protocols, allowing you to take advantage of these protocols without having to change your applications.

- **Security Features**: ALB integrates with AWS Certificate Manager (ACM) for SSL termination, AWS Web Application Firewall (WAF) for protecting your applications from common web exploits, and AWS Cognito for user authentication and authorization.

### Use Cases of ALB

ALB is particularly suitable for load balancing of HTTP and HTTPS traffic, microservices, and container-based applications. You can use ALB to direct user traffic to achieve more efficient resource utilization, better application performance, and improved availability.

Remember, apart from ALB, AWS also offers other types of load balancers like Classic Load Balancer (CLB) and Network Load Balancer (NLB), which are more suited to different use cases.

**Security Tips**
When using ALB you can block all other traffic to your EC2 instance so that all traffic has to come through your Load balancer which can be set up to detect harmful traffic and monitor the health of your EC2 instance