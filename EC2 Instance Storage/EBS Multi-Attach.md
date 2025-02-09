- Support io1 and io2 family
- Multiple ec2 attach to a EBS volume
- Each ec2 instance has permission to read/write
- Use cases: 
	- **Higher application availability** in clustered linux app (teradata)
	- Applicaition that handle concurrent writes
**Note**: 
- Up to **16 EC2** at a time
- Must use cluster-aware file system (not XFS, EXT4,...)