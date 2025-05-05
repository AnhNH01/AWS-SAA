Section start: [[AWS Certified Solutions Architect Slides v40.pdf#page=181|AWS Certified Solutions Architect Slides v40, page 181]]


RDS
- Automated:
	- Daily full backup
	- Transaction log every 5 min (enable point-in-time recovery in said 5 min windows)
	- 1 -> 35 days retention, set to 0 to disable

Aurora
- Automated
	- 1-35 days retention (can not be disabled)
	- Point in time recovery for the whole window

Manual (the same for RDS and Aurora):
- Manually trigger snapshot
- Retention for however long


**Restore option**
General idea is create a backup, store on S3, restore by creating a new db

**Aurora Cloning**
- Use **copy-on-write** protocol
- Suitable for creating a staging db from prod data without affecting the prod db 