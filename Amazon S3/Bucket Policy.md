Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=271|AWS Certified Solutions Architect Slides v40, page 271]]
### Amazon S3 Security

#### **User-Based Security**

- **IAM Policies**: Control which API calls an IAM user can perform.

#### **Resource-Based Security**

- **S3 Bucket Policies**: Bucket-wide rules to grant or deny access (used for cross-account access and making buckets public).
- **Object ACLs**: Fine-grained permissions at the object level (can be disabled).
- **Bucket ACLs**: Less common, provides permissions at the bucket level (can be disabled).

#### **Access Conditions**

- An IAM principal can access an S3 object if **IAM permissions** or **resource policies** allow it and **no explicit deny** exists.

#### **Encryption**

- Objects can be encrypted using encryption keys for additional security.

#### **Bucket Policy Example**

- **JSON-based policies** define:
    - **Resource**: Specifies the bucket and objects it applies to.
    - **Effect**: Allow or Deny actions.
    - **Actions**: API operations permitted (e.g., `s3:GetObject`).
    - **Principal**: Defines who is granted permissions.

#### **Common Use Cases for Bucket Policies**

- Grant **public access** to a bucket.
- Enforce **encryption** on uploaded objects.
- Enable **cross-account access**.

#### **Other Security Settings**

- **Block Public Access Setting**:
    - Prevents buckets from being made public even if a bucket policy allows it.
    - Can be set at the **account level** for global protection.
- **IAM Roles for EC2 Access**:
    - Use **IAM roles** (not IAM users) to grant EC2 instances access to S3.