Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=300|AWS Certified Solutions Architect Slides v40, page 300]]

### Amazon S3 Baseline Performance & Optimization

#### **Baseline Performance**

- **High scalability**: S3 automatically scales to handle high request rates.
- **Low latency**: 100-200ms to retrieve the first byte.
- **Request rate per prefix**:
    - **3,500** PUT/COPY/POST/DELETE per second.
    - **5,500** GET/HEAD per second.
- **Unlimited prefixes**: Performance scales with more prefixes.
    - Example:
        - `/folder1/sub1/file` → 3,500 PUTs & 5,500 GETs per second.
        - `/folder1/sub2/file` → Another 3,500 PUTs & 5,500 GETs per second.
        - Spreading reads across 4 prefixes → **22,000 requests/sec**.

#### **Performance Optimization**

1. **Multi-Part Upload (For Large Files)**
    
    - Recommended for files **>100MB**.
    - Required for files **>5GB**.
    - Splits files into parts and uploads them in parallel for faster transfer.
2. **S3 Transfer Acceleration (For Faster Uploads/Downloads)**
    
    - Uses **AWS Edge Locations** to speed up transfers.
    - Data moves **quickly to a nearby edge location**, then travels via the **AWS private network** to the final S3 bucket.
    - **Reduces reliance on the public internet**, increasing speed and reliability.
    - **Compatible with Multi-Part Uploads**.
    - Example: Uploading from the USA to an S3 bucket in Australia →
        - Data first goes to a US edge location → Faster private AWS network to Australia.
3. **S3 Byte Range Fetches (For Faster Downloads)**
    
    - Allows **parallel GET requests** for specific byte ranges of a file.
    - **Speeds up downloads** by fetching multiple parts simultaneously.
    - **Increases resilience**: If a byte range fails, only that part is retried.
    - **Use case**:
        - Retrieve only part of a file (e.g., first 50 bytes for metadata).
        - Speed up large file downloads with parallel fetching.

#### **Summary**

- **Baseline Performance**: High request rate per prefix, scale with more prefixes.
- **Upload Optimization**:
    - **Multi-Part Upload** → Parallelizes file uploads.
    - **Transfer Acceleration** → Uses Edge Locations to speed up transfers.
- **Download Optimization**:
    - **Byte Range Fetches** → Parallel GET requests for faster retrieval.
- **Key takeaway**: Use **prefix scaling, multi-part uploads, transfer acceleration, and byte range fetches** for optimal S3 performance.