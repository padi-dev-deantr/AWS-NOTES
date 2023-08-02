## Amazon CloudFront

Amazon CloudFront is a web service that speeds up the distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centers called edge locations. 

### Key Features:

- **Edge Locations**: CloudFront uses edge locations around the world to cache copies of your content close to your users, reducing latency.

- **Integration with AWS**: CloudFront is tightly integrated with other Amazon services such as Amazon S3, Amazon EC2, Elastic Load Balancing, Amazon Route 53, and AWS Shield for DDoS protection.

- **Security**: It supports HTTPS for secure delivery of data, and AWS Certificate Manager for managing SSL/TLS certificates. Also, you can configure CloudFront to help protect your application against SQL injection and XSS attacks.

- **Cache & Invalidate Content**: CloudFront caches responses to GET, HEAD, and OPTIONS requests to improve the performance of read-heavy workloads. You can also remove objects from CloudFront cache (invalidate objects) before it expires.

### Use Cases:

- **Websites and Web Applications**: Improve performance and reduce latency by caching static content at edge locations.

- **API Acceleration**: Speed up API calls to backend services hosted on AWS or on-premises.

- **Video Streaming**: CloudFront provides a scalable and secure solution for delivering live and on-demand video to any device.

- **Software Distribution**: Distribute software updates, OS patches, or other digital goods to users around the world.

## AWS Global Accelerator

AWS Global Accelerator is a service that improves the availability and performance of your applications. It provides static IP addresses that act as a fixed entry point to your application endpoints in a single or multiple AWS Regions.

### Key Features:

- **Improve Performance**: By leveraging the AWS global network, it can route user requests through the most optimal network paths.

- **Static IP Addresses**: Global Accelerator provides you with a set of static IP addresses which are anycast from AWS edge locations.

- **Built-in Fault Tolerance**: It reacts instantly to changes in users, application health, and network conditions to ensure that user traffic is directed to a healthy endpoint.

- **DDoS Protection**: It provides inherent DDoS mitigation capabilities and protects your applications against common infrastructure (Layer 3 and 4) attacks.

### Use Cases:

- **Performance Improvement**: Use AWS Global Accelerator to improve the performance of your applications by leveraging the AWS managed global network.

- **Failover**: Enable instant regional failover to secondary regions for high availability.

- **Disaster Recovery**: Redirect user traffic from an unhealthy application endpoint to a healthy endpoint in case of a disaster.

Remember that while both CloudFront and Global Accelerator help to improve the performance of your applications, they serve different purposes. CloudFront is a Content Delivery Network (CDN) service that serves and caches content to end users, whereas Global Accelerator mainly helps to accelerate outbound connections from your workloads in AWS to end users.