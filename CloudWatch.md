# CloudWatch

### what is cloudwatch
CloudWatch is a monitoring service to monitor your AWS resources as well as the applications that you run on AWS.

### what can cloudwatch monitor?
- **compute**
    - ec2 instances
    - autoscaling groups
    - elastic load balancers
    - route 53 health check
- **storage and content delivery**
    - ebs volumes
    - storage gateways
    - cloudfront
- CPU
- Network
- Disk 
- Status Check

### difference between cloudtrail and cloudwatch
cloudtrail increases the visibility into your user and resource activity by recording **AWS Management Console actions** and **API calls**.  You can identify which users and accounts called AWS, the source IP address from which the calls were made, and when the calls occurred. 

- CloudWatch monitors performance

- CloudTrail measures console actions and API calls


### other bits
- cloudwatch is used for monitoring performance
- cloudwatch can monitor most of AWS as well as your applications that run on AWS
- cloudwatch with ec2 will monitor events every 5 minutes by default
- you can have 1 minute intervals by turning on detailed monitoring
- you can create cloudwatch alarms which trigger notifications
- cloudwatch is all about performance.  cloudtrail is about auditing

### other resources
[CloudWatch FAQs](https://aws.amazon.com/cloudwatch/faqs/)



