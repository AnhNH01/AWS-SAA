Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=304|AWS Certified Solutions Architect Slides v40, page 304]]

### **Amazon S3 Storage Lens: Analysis & Optimization**

#### **Overview**

- **S3 Storage Lens** helps analyze, optimize, and protect **storage usage** across an **AWS Organization**.
- Detects **anomalies**, identifies **cost efficiencies**, and ensures **best practices**.
- Provides **30-day usage and activity metrics**, aggregating data at different levels:
    - **Organization-wide**
    - **Accounts**
    - **Regions**
    - **Buckets**
    - **Prefixes**
- Supports **default & custom dashboards**.
- **Exports reports** in **CSV/Parquet** formats to an S3 bucket.

---

### **Key Features & Metrics**

#### **1. Default Dashboard**

- **Pre-configured by AWS** (cannot be deleted, only disabled).
- **Aggregates data** across accounts & regions.
- **Displays key storage insights**, including:
    - **Total storage usage**
    - **Object count**
    - **Average object size**
    - **Number of buckets & accounts**
- **Custom filters** for regions, accounts, buckets, storage classes, etc.

#### **2. Storage Lens Metrics Categories**

| **Metric Type**               | **Purpose**                      | **Key Metrics**                                                         | **Use Cases**                                                                              |
| ----------------------------- | -------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| **Summary Metrics**           | General storage insights         | Total storage bytes, object count                                       | Identify unused or rapidly growing buckets                                                 |
| **Cost Optimization Metrics** | Reduce storage costs             | Non-current version storage bytes, incomplete multi-part uploads        | Clean up old versions, failed uploads, or transition objects to lower-cost storage classes |
| **Data Protection Metrics**   | Enforce security & compliance    | Versioning enabled, MFA Delete, SSE-KMS, cross-region replication rules | Identify non-compliant buckets                                                             |
| **Access Management Metrics** | Manage bucket ownership & access | Object ownership settings                                               | Check ownership settings across buckets                                                    |
| **Event Metrics**             | Monitor event notifications      | Count of buckets with S3 event notifications                            | Ensure event-driven workflows are set up properly                                          |
| **Performance Metrics**       | Optimize transfer performance    | S3 Transfer Acceleration enabled count                                  | Identify performance optimizations                                                         |
| **Activity Metrics**          | Track storage usage & requests   | GET/PUT requests, bytes downloaded, etc.                                | Analyze request patterns & optimize access                                                 |
| **HTTP Status Code Metrics**  | Monitor access patterns & errors | 200 OK, 403 Forbidden, etc.                                             | Identify potential access issues                                                           |

---

### **Free vs. Paid Metrics**

|**Feature**|**Free Metrics**|**Advanced (Paid) Metrics**|
|---|---|---|
|**Number of metrics**|28 usage metrics|Additional activity, cost, protection, and status code metrics|
|**Data retention**|14 days|15 months|
|**CloudWatch integration**|❌ No|✅ Yes (CloudWatch access)|
|**Prefix-level metrics**|❌ No|✅ Yes (bucket-level and prefix-level analysis)|

---

### **Key Takeaways for the Exam**

✅ **Storage Lens provides organization-wide storage insights** across multiple accounts & regions.  
✅ **Default dashboard is pre-configured and cannot be deleted.**  
✅ **Free vs. Paid**: Free offers **basic storage metrics**, Paid provides **advanced insights & CloudWatch integration**.  
✅ **Key Use Cases**: Cost optimization, security compliance, performance monitoring, and activity tracking.  
✅ **Exports reports in CSV/Parquet format** for further analysis.
