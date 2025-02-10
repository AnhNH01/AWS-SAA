
[[CIDR, IP]]
**Note**: Max CIDR per VPC is 5
- Smallest is /28 (16 IPs)
- Biggest is /16 (65536 IPs)

**Note**: When creating a new subnet, AWS will reserve 5 IPs (First 4 & Last)

[[Transit Gateway]]
**Note**: The **ONLY** AWS service that support **multicast**

[[Elastic Block Storage]]
**Note**: Delete on termination -> control the behavior of EBS when the EC2 instance it is attached to is terminated. 
- For **root** volume -> Default **enable**
- For other volume -> Default **disable**

[[EBS Multi-Attach]]
**Note**: 
- Up to **16 EC2** at a time
- Must use cluster-aware file system (not XFS, EXT4,...)

[[NLB (Network Load Balancer)]]
**Note**
- Health check supports 3 protocols: HTTP, HTTPs, TCP. 
- NLB has **one static IP per AZ** and support assigning Elastic IP.

[[GWLB (Gateway Load Balancer)]]
**Note**: **GENEVE** protocol, port **6801**