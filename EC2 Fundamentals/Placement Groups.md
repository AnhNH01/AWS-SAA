*Controls how the EC2 instances are deployed physically*'

**Cluster**
![[ec2-placement-group-cluster.png]]

- All in the same AZ, connected by high throughput network (^10 Gbps)
- Can be subjected to simultaneous failure
- Use cases: Jobs that need low latency

**Spread**

![[placement-group-spread.png]]

- Spread across multiple AZ, maximum 7 instances per AZ per group
- Each instance is placed on different hardware -> reduce risks of simultaneous failure 
- Use cases: Critical jobs that needs to maximize HA, need isolated failure

**Partition**
- Spread across multiple AZ in the same region, a partition ~ a rack
- Can scale up to 100s of instances
- Failure is isolated to racks
- Use cases: Partition-aware job (HDFS, Cassandra, Kafka...)