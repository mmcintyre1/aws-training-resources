## Cloudfront
### What is a CDN?
A content delivery network (CDN) is a system of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage, and a content delivery server

Cloudfront is AWS's CDN.  

### Key Items
- **Edge Location** - location where content will be cached
- **Origin** - origin of files that CDN will distribute (S3 bucket, EC2, ELB, or Route53)
- **Distribution** name given to CDN/Edge Locations
- 

### something like a sales pitch
Cloudfront can be used to deliver entire website including dynamic, static, streaming, and interactive content using a global network of edge locations.  Request for your content are automatically routed to the nearest edge location, so content is delivered with the best possible performance

### two ways to distribute
- Web distribution typically for websites
- RTMP used for media streaming

### other bits
- Edge locations aren't read only 
- objects are cached for the life of the TTL (time to live)
- you can clear cached objects (invalidate) but you will be charged

### other resources
[Cloudfront FAQs](https://aws.amazon.com/cloudfront/faqs/)
