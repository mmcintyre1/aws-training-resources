# Networking (ENI, ENA, EFA)

### ENI 
elastic network interface - essentially a virtual network card

##### use cases
- create a management network
- use network and security appliances in your VPC
- create dual-homed instances with workloads/roles on distinct subnets
- create low-budget, high-availability solution

### EN(A)
enhanced networking -- uses single root i/o virtualization (SR-IOV) to provide high-performance networking capabilities on supported instance types.

##### use cases
- higher bandwith, higher packet per second (PPS) performance, and consistently lower inter-instance latencies
- there is no additional charge for using enhanced networking (EC2 instance needs to support )
- if you want good network performance

In any scenario question, you want to choose ENA over VF if given the option

### EFA
elastic fabric adapter - a network device that you can attach to your EC2 instance to accelerate high performance computing (HPC) and machine learning applications

##### use cases
- provides lower and more consisten latency and higher throughput than the TCP transport traditionally used in cloud-based HPC systems
- EFA can use OS-bypass, which enables HPC and machine learning applications to bypass the os kernel and communicate directly with the EFA device -- this mkaes it a lot faster and lower latency (only supported on linux)


#### final bits
**ENI**
for basic netowrking.  perhaps you need a separate management network to your production network or a separate logging network and you need to do this at low cost

**EN**
for when you need speeds between 10 Gbps and 100 Gbps.  anywhere you need reliable, high throughput

**EFA**
for when you need to accelerate high performance computing (HPC) and machine learning applications *or* if you need to do an OS bypass
