## S3 notes

### top level notes
 - s3 buckets are object-based: i.e. allows you to upload files
 - files can be from 0 bytes to 5 TB
 - there is unlimited storage
 - files are stored in buckets
 - S3 is a universal namespace (names must be unique globally)
    - this is because S3 names are actually pathed out network locations, e.g. https://mycloudinstance.s3.amazonaws.com
 - Not suitable to install an OS or DB on (you'd want block-based storage for that)
 - successful uploads will generate an HTTP 200 status code
 - you can turn on MFA delete
 - you can control access to buckets using **bucket ACL** or using **bucket policy**

### key fundamentals
- `Key` the name of the object
- `Value` the sequence of bytes
- `Version ID` important for versioning
- `Metadata` data about the object
- `Subresources`
   - `access control lists`
   - `torrents`

### consistency model
- Read after Write consistency for PUTS of new Objects
- Eventual Consistency for overwrite PUTS and DELETES 


### storage classes
1. **S3 Standard**
99.99% availability
99.999999999% durability
stored redundantly across multiple devices in multiple ffacilities and is designed to sustain the loss of 2 facilities concurrently

2. **S3- IA (Infrequently accessed)**
For data that is accessed less frequenlty but requires rapid access when needed
Lower fee than S3 but you are charged a retrieval fee

3. **S3 One Zone - IA** ***aka S3 RRS***
For where you wawnt a lower-cose option for infrequently accessed data but do not require multiple AZ data resiliency

4. **S3 - Intelligent Tiering**
Designed to optimize costs by automatically moving data to the most cost-effectiove access tier without performance impact or operational overhead

5. **S3 Glacier**
secure, durable and low-cost storage class for data archiving.  Retrieval times configurable from minutes to hours

6. **S3 Glacier Deep Archive**
Lowest cost storage class where a retrieval time of 12 hours is acceptable

![image](https://github.com/mmcintyre1/aws-training-resources/blob/master/images/s3-comparison.PNG)

### what makes up the cost of S3?
- storage
- requests and data retrieval 
- data transfer
- managament and replication

### how to get the best value?
- S3 Standard > S3 IA > S3 Intelligent Tiering > S3 One Zone IA > S3 Glacier > S3 Glacier Deep Archive'
- Normally try and get to S3 Intelligent Tiering

### S3 security & encryption
##### Encryption in Transit (e.g. HTTPS)
 - SSL/TLS
##### Encryption at Rest (Server-Side)
- S3 Managed Keys - SSE-S3
- AWS Key Management Service, Managed Keys - SSE-KMS
- Server Side Encryption with Customer Provided Keys - SSE-C

##### Encryption at Rest (Client Side)
- Encrypted locally before transfer to S3

### External Resources
[S3 FAQs](https://aws.amazon.com/s3/faqs/)
