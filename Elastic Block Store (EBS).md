# EBS
### What is EBS?
amazon elastic block store provides persistent block storage volumes for use with Amazon EC2 instances in the AWS Cloud.  Each EBS volume is automatically replicated within its AZ to protect you from component failure, offering high availability and durability.

### types
1. General Purpose (SSD)
2. Provisioned IOPS (SSD)
3. Throughput Optimized HDD 
4. Cold HDD
5. Magnetic

![image](https://github.com/mmcintyre1/aws-training-resources/blob/master/images/ebs-types.png)

### how do you change AZ?
- create snapshot and create image (AMI) from EBS snapshot
- make sure that virtualization type is hardware-assisted virtualization (HVM) which allows for more flexibility for instance type when creating from image later
- when you launch you can pick new subnet (AZ)
- you can also copy AMI from existing region to new region

### other stuff
- EBS will be in same AZ as EC2 instance
- cant make volume smaller, only larger
- OS might not see full storage (need to be repartitioned)
- EBS attached volumes persist beyond EC2 termination
- snapshots are stored on S3
- snapshots are point in time copies of volumes
- snapshots are incremental - only blocks that have changed since you last snapshots are moved to S3
- to create a snapshot for EBS volume that is root, best practice to stop the instance before taking the snapshot

### other resources
[EBS FAQs](https://aws.amazon.com/ebs/faqs/)
