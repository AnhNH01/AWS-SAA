Slide:[[AWS Certified Solutions Architect Slides v40.pdf#page=266|AWS Certified Solutions Architect Slides v40, page 266]]

- Amazon S3 (Simple Storage Service) is a highly scalable storage solution.
- Used for web hosting, backup, disaster recovery, and data lakes.
- Many AWS services and major companies rely on S3.

#### **Use Cases**

- Backup and disaster recovery (data replication across regions).
- Archival storage (e.g., S3 Glacier for long-term retention).
- Hybrid cloud storage (extending on-prem storage to the cloud).
- Hosting applications, media files, and static websites.
- Data lakes and big data analytics.
- Delivering software updates.

#### **Buckets & Objects**

- S3 stores files in **buckets** (top-level directories).
- Files inside buckets are called **objects**.
- Each bucket must have a **globally unique name** across all AWS accounts.
- Buckets are created in a **specific AWS region**.

#### **Bucket Naming Rules**

- No uppercase letters or underscores.
- Length: 3 to 63 characters.
- Cannot be an IP address.
- Must start with a lowercase letter or number.
- Can use letters, numbers, and hyphens.

#### **Objects & Keys**

- Objects (files) have a **key**, which is their full path.
- S3 does not have actual directories; it uses **prefixes** to simulate folder structures.
- `s3://my-bucket/folder/child-folder/my-file.txt`

#### **Object Details**

- **Max object size:** 5 TB.
- **Files >5 GB:** Must use **multi-part upload** (splitting into smaller parts).
- **Metadata:** Key-value pairs for additional object information.
- **Tags:** Up to 10 per object, useful for security and life cycle management.
- **Versioning:** Each object can have a **version ID** if versioning is enabled.