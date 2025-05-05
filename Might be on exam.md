
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

**Note:**
- EBS supports fast snapshot and restore (billed by the minute)

[[EBS Multi-Attach]]
**Note**: 
- Up to **16 EC2** at a time
- Must use cluster-aware file system (not XFS, EXT4,...)

[[ALB (Application Load Balancer)]]
**Note**: ALB heath check support HTTP and HTTPs

[[NLB (Network Load Balancer)]]
**Note**
- Health check supports 3 protocols: HTTP, HTTPs, TCP. 
- NLB has **one static IP per AZ** and support assigning Elastic IP.
- Run on L4
- NLB supports HTTP health check but can only use ec2 instance or IP as endpoint (not url)

[[GWLB (Gateway Load Balancer)]]
**Note**: 
- **GENEVE** protocol, port **6801**
- Manage 3rd party appliances
- Run on L3 (Network Layer)


[[RDS Read Replicas vs MultiAZ]]
**Note**: Read replicas can be setup as multiAZ for disaster recovery (DR)

**Note**: RDS single AZ to multi AZ is a zero-downtime operation. You just click modify and enable multi AZ.
Internally:
- Snapshot will be taken
- Restore to another AZ
- Sync the two database


Amazon Aurora Advanced Concepts
**Note**: Typical cross-region replication takes less than 1 second in **global Aurora database**.

[[RDS & Aurora - Backup and monitoring]]
**Note**: You still need to pay for storage even if an RDS db is stopped. If you plan to stop for a long time, use backup & restore instead, the costs for snapshots are lower. 

**Note**: You can **NOT** create new encrypted read-replicas from unencrypted rds instance

[[RDS Proxy]]
**Note**: Improving database efficiency by decreasing stress on DB resorces (CPU, RAM) and minimize open connection (and timeouts)

**Note**: Reduce failover time by up to 66% when using RDS proxy

**Note**: Enforce IAM Authentication for DB, securely store instance credentials in AWS Secrets Manager

**Note**: RDS Proxy is never publicly accessible, only available from the VPC

[[S3]]
**Note**: Batch operation can be use to encrypt all unencrypted files

**Note**:
- **Unpredictable** access pattern -> most likely should use **intelligent tiering**.
- S3 event can only target **1 destination at a time**. If you want multiple destination simultaneously, choose s3 -> event bridge -> des.

AWS Quicksight
**Note:** Should manage access using QuickSight users and groups


AWS Config
**Note**:
- Record and audit **compliance of AWS Resources**


AWS Trusted Advisor
**Note**:
- Evaluate based on AWS Well-architected frameworks

AWS Inspector
**Note**:
- Inspect vul of EC2, lambda, container images


AWS Cloudwatch
**Note**:
- You can share the dashboard on the console (least privileged principle)
- You can config **log subscription** to get access to real-time CW log event from other AWS services

AWS Active Directory
**Note**:
- Need **two-way** trust forest when connect Identity center with self-managed ADs.

AWS AppFlow
**Note**:
- Securely transfer data between **SaaS** and AWS


Systems Manager
- Can be used to run commands on multiple instances
- Patch Manager is used to **automate, schedule** maintenance windows

AWS CloudFront
- Can be used to serve dynamic data also. When used, traffic for dynamic data is moved to the AWS network



S3 Object Lock
- Governance mode: restrict **most** user from altering for predefined time (retention policy)
- Compliance mode: restrict **all**, even root for predefined time (retention policy)
- Legal hold: (use for time setting) -> if you are unsure about the retention period