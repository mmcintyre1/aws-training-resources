# AWS Well-Architected Framework

five pillars

1. operational excellence
2. security
3. reliability
4. performance efficiency
5. cost optimization


#### some terminology
`component`: unit of technical ownership

`workload`: set of components that work together

`milestone`: key changes in architecture (design, go-live, etc)

`technology portfolio`: collection of workloads that make up business operations


NTS: What is the TOGAF or Zachman framework?

#### good design principles
a. stop guessing capacity needs
b. test systems at production scale
c. automate to make architectural experimentation easier
d. allow for evolving architecture
e. drive architectures through data
f. improve through 'game days'


## Operational Excellence
### Overview
The ability to run and monitor systems to deliver business value and to continually improve supporting processes and proecdures


### Design Principles
1. perform operations as code
2. annotate documentation
3. make frequent, small, reversible changes
4. refine operations procedures frequently
5. anticipate failure
6. learn from all operational failures


### Best Practices
1. Prepare
	- how do you determine what your priorities are?
	 - how do you design your workload so that you can understand its state?
	- how do you reduce defects, ease remediation, and improve flow into production?
	- how do you mitigate deployment risks?
	- how do you know you are ready to support a workload?
  
2. Operate
	- how do you understand the health of your workload?
	- how do you understand the health of your operations?
	- how do you manage workload and operation events?
  
3. Evolve
	- how do you evolve operations?



## Security
### Overview
The ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies

### Design Principles
1.  implement a strong identity foundation
2.  enable traceability
3.  apply security at all layers
4.  automate security best practices
5.  protect data in transit and at rest
6.  keep people away from data
7.  prepare for security events

### Best Practices
1. Identity and Access Management
	- how do you manage credentials and authenetication?
	- how do you control human access?
	- how do you control programmatic access?
  
2. Detective Controls
	- how do you detect and investigate security events?
	- how do you defend against emerging security threats?
  
3. Infrastructure Protection
	- how do you protect your networks?
	- how do you protect your compute resources?
  
4. Data Protection
	- how do you classify your data?
	- how do you protect your data at rest? 
	- how do you protect your data in transit?
  
5. Incident Response
	- how do you respond to an incident?

## Reliability
### Overview
The ability of a system to recover from infrastructure or service disruptions, dynamically acquire computer resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues. 
### Design Principles
1. test recovery procedures
2. automatically recover from failure
3. scale horizontally to increase aggregate system availability
4. stop guessing capacity
5. manage change in automation
### Best Practices
1. Foundations
    - how do you manage service limites?
    - how do you manage you network topology?
    
2. Change Management
    - how does your system adapt to changes in demand?
    - how do you monitor your resources?
    - how do you implement change?
    
3. Failure Management
    - how do you backup data?
    - how does your system withstand component failures?
    - how do you test resilience?
    - how do you plan for disaster recovery?

## Performance Efficiency
### Overview
The ability to use computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technnologies evolve.
### Design Principles
1. democratize advanced technologies
2. go global in minutes
3. use serverless architecture
4. experiment more often
5. mechanical sympathy
### Best Practices
1. Selection
    - how do you select the best performing architecture?
        - how do you select your compute solution?
        - how do you select your storage solution?
        - how do you select your database solution?
        - how do you configure your networking solution?
        
2. Review
    - how do you evolve your workload to take advantage of new releases?
    
3. Monitoring
    - how do yopu onitor your resources to ensure they are performing as expected?
    
4. Tradeoffs
    - how do you use tradeoffs to improve performance?

## Cost Optimization
### Overview
The ability to run systems to deliver business value at the lowest price point.
### Design Principles
1. adopt a consumption model
2. measure overall efficiency
3. stop spending money on data center operations
4. analyze and attribute expenditure
5. use managed and application level services to reduce cost of ownership
### Best Practice
1. Expenditure Awareness
    - how do you govern usage?
    - how do you monitor usage and cost?
    - how do you decommission resources?
    
2. Cost-Effective Resources
     - how do you evaluate cost when you select services?
     - how do you meet cost targets when you select resource type and size?
     - how do you use pricing models to reduce cost? 
     - how do you plan for data transfer charges?
     
3. Matching Supply and Demand
    - how do you match supply of resources with demand?
    
4. Optimizing over Time 
    - how do you evaluate new services?

