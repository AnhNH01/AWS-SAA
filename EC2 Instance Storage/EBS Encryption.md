When you encrypt an EBS volume, all things will be encrypted:
- Data inflight
- Data at rest
- Snapshot
- Volumes created from the snapshot

Encryption has minimal effect on latency

Use KMS (AES 256)


**How to Encrypt a non-encrypted EBS volume** 
-> Basically you have to create a encrypted copy

- Create a snapshot
- Copy that snapshot (and choose to encrypt)
- Create a encrypted volume from encrypted snapshot (or can create a encrypted volume from unencrypted snapshot)
- Attach the encrypted volume in place of original volume