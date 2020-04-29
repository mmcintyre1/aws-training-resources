# VPC

### what is vpc
amazon virtual private cloud lets you provision a logically isolated section of the aws cloud where you can launch aws resources in a virtual netowrk that you define.  you have complete control over your virtual networking environment, including selection of your own ip address range, creation of subnets, and configuration of route tables and network gateways. 

### creating a vpc
- when you create a VPC a route table, a network access control list and a default security group
- no subnets or internet gateways will be created

### subnets
- one subnet == one availability zone
- amazon reserve 5 ip addresses within subnet

### internet gateway
- only one internet gateway per VPC

### security groups
- security groups can't span VPCs

### route tables

### NAT Gateways
- Network Address Translation
- allows your instances in private subnets to communicate with the internet
- redundant within the AZ
- scales automatically
- no need ot patch
- not associated with security Groups
- automatically assigned a public IP address 
- just need to update Route Table
- If you have resources in multiple AZs and they share one NAT gateway, in the event that the NAT gateway's AZ is down, resources in the other AZs lose internet access.  To create an AZ-independent architecture, create a NAT gateway in each AZ and configure your routing to ensure that resources use the NATE gateway in the same AZ.

### Network Access Control List
- your VPC automatically cvomes with a default network ACL and by default it allows all outbound and inbound traffic
- you can create a custom network ACL -- by default an ACL denies all inbound and outbound traffic until you add rules
- each subnet in your VPC must be associated with a network ACL.  If you don't explicitly associate a subnet with a network ACL the subnet is automatically associated with the default network ACL
- you can block IP address uses the network ACL but not security groups
- you can associate a network ACL with multiple subnets; however, a subnet can be associated with only one network ACL at a time.  When you assoicate a netwrok ACL with a subnet the previous association is removed
- netwrk ACLs contain a numbered list of rules that is evaluated in order, starting with the lowest numbered rule
- network ACLs have separate inbound and outbound rules, and each rule can either allow or deny traffic
- network ACLs are stateless -- responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa)

### other bits
- us-east-1a in your aws instance can be completely different than a different account -- az's are randomized


### Other Resources
[AWS VPC FAQs](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
