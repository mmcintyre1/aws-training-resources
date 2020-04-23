## Identity Access Management
Tool to manage users, groups, policies, and roles and their access levels

### what does IAM do?
- centralized control of AWS account
- shared access to AWS account
- granular permissions
- identity federation (including AD, Facebook, etc.)
- MFA
- temporary access for users/devices and services where necessary
- alllows you to set up password rotation policy
- integrates with many different AWS services
- supports PCI DSS compliance (credit card info storage)

### top level notes
- IAM is universal and does not apply to regions individually (at this time)
- The "root account" is the account created when first setup your AWS accout and has complete admin access
- new users have **NO** permissions when initially created
- New users are assigned `Access Key ID` and `Secret Access Key` when given programmatic access
- These cannot be used to log in to the console -- only the created password can be
- always set up MFA on root account
- you can create and customize password rotation policies

### IAM key terms
- **Users** - End users such as people, employees of an organization
- **Groups** - A collection of usrs -- each user in the group will inherit the permissions of the group
- **Policies** - Policies are made up of documents called Policy documents.  These documents are in JSON and give permissions to what a User/Group/Role is able to do
- **Roles** - You create roles and then assign them to AWS Resources
