Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=282|AWS Certified Solutions Architect Slides v40, page 282]]

 **S3 Standard (General Purpose)**  
   - **Availability:** 99.99%  
   - **Use Cases:** Frequently accessed data, big data analytics, mobile and gaming applications, content distribution  
   - **Features:** Low latency, high throughput, sustains 2 concurrent facility failures  

2. **S3 Standard-IA (Infrequent Access)**  
   - **Availability:** 99.9%  
   - **Use Cases:** Disaster recovery, backups  
   - **Features:** Lower cost than Standard, retrieval cost applies, rapid access when needed  

3. **S3 One Zone-IA**  
   - **Availability:** 99.5%  
   - **Use Cases:** Secondary backups, data that can be recreated  
   - **Features:** High durability but stored in a single AZ, data loss possible if AZ is destroyed  

4. **S3 Glacier Instant Retrieval**  
   - **Availability:** High  
   - **Use Cases:** Archival storage, accessed once per quarter  
   - **Features:** Low cost, retrieval in milliseconds, minimum storage duration of 90 days  

5. **S3 Glacier Flexible Retrieval**  
   - **Availability:** High  
   - **Use Cases:** Long-term archival storage with flexible retrieval times  
   - **Features:**  
     - Expedited: 1-5 min retrieval  
     - Standard: 3-5 hours  
     - Bulk: 5-12 hours (free)  
     - Minimum storage duration: 90 days  

6. **S3 Glacier Deep Archive**  
   - **Availability:** High  
   - **Use Cases:** Long-term archival with infrequent access  
   - **Features:**  
     - Standard: 12-hour retrieval  
     - Bulk: 48-hour retrieval  
     - Lowest cost, minimum storage duration of 180 days  

7. **S3 Intelligent-Tiering**  
   - **Availability:** High  
   - **Use Cases:** Automatically moves objects between tiers based on access patterns  
   - **Features:**  
     - Frequent Access Tier (default)  
     - Infrequent Access Tier (objects unused for 30 days)  
     - Archive Instant Access Tier (objects unused for 90 days)  
     - Archive Access Tier (configurable from 90+ days)  
     - Deep Archive Access Tier (configurable from 180+ days)  
     - Small monthly monitoring and auto-tiering fee, **no retrieval charges**  

#### **Durability & Availability**  
- **Durability:** 99.999999999% (11 nines) across all storage classes  
- **Availability:** Varies by storage class (higher for frequently accessed data)  

#### **Storage Class Selection**  
- Objects can be **assigned a class at creation** or **moved using S3 Lifecycle rules**.