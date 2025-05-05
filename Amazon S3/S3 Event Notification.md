Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=297|AWS Certified Solutions Architect Slides v40, page 297]]
#### **What Are S3 Events?**

- Events occur in Amazon S3 when actions happen, such as:
    - **Object Created**
    - **Object Deleted**
    - **Object Restored**
    - **Replication Events**
- Events can be **filtered** (e.g., only trigger for `.jpeg` files).

#### **Use Case**

- **Automatically react** to S3 events.
- Example: Generate thumbnails when images are uploaded.

#### **Event Destinations**

S3 event notifications can be sent to:

1. **SNS (Simple Notification Service)**
2. **SQS (Simple Queue Service)**
3. **AWS Lambda**

#### **IAM Permissions for Event Notifications**

- **SNS Topic** → Requires an **SNS resource access policy** to allow S3 to publish messages.
- **SQS Queue** → Requires an **SQS resource access policy** to allow S3 to send messages.
- **Lambda Function** → Requires a **Lambda resource policy** to allow S3 to invoke the function.

#### **Amazon EventBridge Integration**

- **All S3 events automatically go to EventBridge.**
- From **EventBridge**, events can be sent to **over 18 AWS services** (e.g., Step Functions, Kinesis, Firehose).
- **Advanced filtering**: Filter by metadata, object size, name, etc.
- **Additional features**: Archive events, replay events, and improve reliability.

#### **Summary**

- **S3 Event Notifications** allow automatic responses to S3 events.
- **Destinations**: SNS, SQS, Lambda, and EventBridge.
- **Permissions**: Resource policies must be attached to SNS, SQS, and Lambda.
- **EventBridge** enhances capabilities with better filtering, multiple destinations, and event archiving.