# Route 53
- dns is on port 53 (thus the name)

### what is dns
- used to convert human friendly domain names into an ipv4 or ipv6 address
- ipv4 is a 32 bit field which has over 4 billion addresses
- ipv6 is 128 bit field which has over 340 undecillion addresses

### glossary
- SOA records
- NS records
- A records
- CNAMES
- MX records
- PTR records

### top level domains
- last word in a domain name is top level domain (.com, .edu)
- second to last is second level domain name (*.co*.uk)
- top level domains are controlled by internet assigned numbers authority (IANA)
- all domain names have to be unique, so domain registrar exists to be an authority to assign domain names directly under on or more top level domain
- domains are registered with the interNIC a service of ICANN, which enforces the uniqueness of domain names
- these domain names are registered in a central database known as a whois database
- every domain name begins with SOA (start of authority), which contains: 
    - the name of the server that supplied the data for the zone
    - the administrator of the zone
    - the current version of the data file
    - the default number of second the the time-to-live file on resource records
- NS record (Name Server) used to top level domain servers to direct traffic to the Content DNS server which contains the authoritative DNS records

![image](https://github.com/mmcintyre1/aws-training-resources/tree/master/images/dns-flow.png)

### TTL
- the length that a DNS record is cached on either the Resolving Server or the users own local PC is equal to the value of the time-to-live in seconds. The lower the TTL, the faster changes to DNS records take to propagate throughout the internet.

- default is 48 hours

### DNS records
- Arecord - an alias record used to map records in your hosted zone to elastic load balancers, cloudfront distros, or S3 buckets that are configured as websites
- CName - a canonical name can be used to resolve one domain name to another
- a CName can't be used for naked domain names (zone apex record)
- if there is a choice between A record and CNAME, choose A record

### routing policies
- `simple routing`
    - you can only have one record with multiple IP addresses
    - if you specify multiple values in a record, route 53 returns all values to the user in a random order
- `weighted routing`
    - allows you to split your traffic based on different weight 
- latency-based routing
- failover routing
- geolocation routing
- geoproximity routing (traffic flow only)
- multivalue answer routing

### other bits
- you can buy domain names from AWS
- and it might take 3 days register depending on circumstances

### other resources
[Route 53 FAQs](https://aws.amazon.com/route53/faqs/)
