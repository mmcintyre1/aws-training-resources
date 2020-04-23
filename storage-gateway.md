## Storage Gateway
### what is storage gateway?
a service that connects to an on-prem software appliance with cloud-based storage to provide seamless and secure integration between an organization's on-prem IT environment and AWS's storage infrastructure.  The service enables you to securely store data to the AWS cloud for scalable and cost-effective storage.

### another sales pitchy thing
software appliance is available for download as a virtual machine (VM) image that you install on a host in your datacenter.  Storage Gateway supports either VMware ESXi or Microsoft Hyper-V ans the hypervisor.  Once you've installed your gatewayt and associated it with your AWS account through the activation process, you can use the AWS Management Console to create the storage gateway option that is right for you

### three different types
1. File Gateway (NFS & SMB)
Files are stored as objects in your S3 buckets, accessed through a Network File System (NFS) mount point.  Ownership, permissions, and timestamps are durable stored in S3 in the user-metadata of the object associated with the file.  Once objects are transferred to S3, they can be managed as native S3 objects, and bucket policies such as versioning, lifecycle management, and cross-region replication apply directly to objects stored in yyour bucket. 

2. Volume Gateway (iSCSI)
The volume interface presents your applications with disk volumes using the iSCSI block protocol.  
Data written to these volumes can be asynchronously backed up as a point-in-time snapshot of your volumes and stored in the cloud as Amazon EBS snapshots.
Snapshots are incremental backups that capture only changed blocks.  All snapshot storage is also compressed to minimize your storage charges.
    - stored volumes
        - entire data set locally
    - cached volumes
       - partial data stored locally (most actively used cached)

3. Tape Gateway (VPTL)
offers durable, cost-effective solution to archive your data in the AWS cloud.  The VTL interface it provides lets you leverage your existing tape-based backup application infrastructure to store data on virtual tape cartridges that you create on your tape gateway.  Each tape gateway is preconfigured with a media changer and tape drives, which are available to your existing client backup applications as iSCCI devices.  You add tape cartridges as you need to archive your data.  Supported by NetBackup, Backup Exec, Veeam, etc.

### the important bits
1.  File Gateway - for flat files stored directly on S3
2.  Volume Gateway
    - stored volumes - entire dataset is stored on site and is asynchronously backed up to S3
    - cached volumes - entire dataset is stored on S3 and the most frequently accessed data is cached on site
3. Gatweway Virtual Tape Library - for tapes

### other resources
[Storage Gateway FAQs](https://aws.amazon.com/storagegateway/faqs/)
          
