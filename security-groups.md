# security groups
- changes in security groups propagate immediately
- security groups are stateful -- if you allow things inbound, it will automatically be allowed outbound
- network access control lists (NACL) are stateless - inbound and outbound rules need to be created
- no way of blacklisting a port or IP address
- you can attach multiple security groups to same EC2 instance (any conflicting rules?)
- all inbound traffic is blocked by default
- all outbound traffic is allowed
- you can have any amount of ec2 instances within security group
