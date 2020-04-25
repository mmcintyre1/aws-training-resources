# WAF

### what is WAF
AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to cloudfront, an application load balancer, or api gateway

it allows you to control access to your content (layer 7 aware)

allows behavior
1. allow all requests except the ones you specify
2. block all requests you except the ones you specify
3. count the requests that match the properties you specify

### some bits
how to block IP addresses, or block individual countries, or sql injection, use WAF.

[WAF FAQs](https://aws.amazon.com/waf/faq/)
