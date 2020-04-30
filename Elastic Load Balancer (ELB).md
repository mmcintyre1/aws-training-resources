# Elastic Load Balancer
- `application load balancers` are suited for load balancing of HTTP and HTTPS traffic -- they opoerate at Layer 7 and are application-aware.  You can create advanced request rotuing, sending specified requests to sepcific locations
- `network load balancers` are best suited for load balancing of TCP traffic where extreme performance is required.  Operating at connection level (layer 4), they are best suited to handling millions of requests per second while maintaining ultra-low latencies
- `classic load balancers` are the legacy elastic load balancers.  you can load HTTP/HTTPS applications and use Layer 7-specific features, such as X-forwarded and sticky sessions.  You can also use strict Layer 4 load balancing for applications that rely purely on the TCP protocol
- 504 error means a gateway has timed out
- troubleshoot the application -- is this the web server or the database server?
- load balancers have their own DNS names -- you are never given an IP address

### sticky sessions
- classic load balancer routes each request indepenedently to the registered EC2 instance with the smallest load
sticky sessions allow you to bind a user's session to specific EC2 instance.  - This ensures that all requests from the user during the session are sent to the same instance
- You can enalbe for ALB but traffic will be sent to the Traffic Group Level
 
### cross zone load balancing
- sends traffic across AZs

### path patterns
- you can create a listener to forward requests based on the URL path


