# EC2

### What is EC2
Amazon Elastic Compute Cloud is a web service that provides resizable compute capacity in the cloud.  Amazon EC2 reduces the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computer requirements change.

### glossary
- AMI - amazon machine image

### how is EC2 priced?
pay as you go, pay for what you use, pay less as you use more, and pay even less if you reserve capacity

### pricing models
1. **on-demand** - allows you to pay fixed rate by the hour with no commitment
    - low cost and flexibility without upfront payment
    - applications with short-term, spiky, or unpredictable workloads that cannot be interrupted
    - applications being developed on EC2 for the first time
2. **reserved** - capacity reservation with a significant discount on hourly charge with 1 or 3 year contracts
    - applications with steady state
    - predictable usage
    - make up front payments
3. **spot** - enables you to bid whatever price you want, providing your applications have flexible start and end times
    - flexible start and end times
    - apps that are only feasible at very low compute prices
    - urgent compute needs for large amounts of additional capacity
4. **dedicated hosts** - physical EC2 server dedicated hosts
    - regulatory requirements
    - licensing problems against multitenancy
    - can be purchased on-demand (hourly)
    - can be purchased as a reservation


### some bits
- root device volumes can be encrypted
- termination p[rotection is turned off by default, you must turn it on
- on an EBS backed instance, the default action is for the root EBS volume to be - deleted when the instance is terminated
- EBS root volumes of your defautl AMIs can be encrypted -- you can also use a - third party app to encryt
- additional volumes can be encrypted

### ami types
you can select ami on 
- region 
- os 
- architecture (32 or 64)
- launch permissions
- storage for root device
    - instance store (ephemeral storage)
    - ebs backed volumes

**EBS Volumes**
- the root device for an instance launched from the AMI is an AMazon EBS volume created from an Amazon EBS snapshot

**Instance Store Volumes**
- the root device for an instance launched from the ami is an instance store volume created from a template stored in Amazon S3
- can't add additional stores later
- can't stop instance-backed volume ec2, so stopping will eliminate all data (ephemeral)

