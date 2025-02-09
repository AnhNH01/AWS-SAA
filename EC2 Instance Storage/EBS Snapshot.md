
- Since [[Elastic Block Storage]] is AZ bound, we can create back up (snapshot) of EBS and then copy them to different AZ -> That is how you can move EBS volume to different AZ
- Best practice is to detach volume while creating snapshot

![[transfer-ebs-accross-AZ.png]]

**Features**

- EBS Snapshot archive: Move some snapshots to archive tier (cheaper ~75%), long restore time (24 -72h)
- Recycle Bin: retention after delete (1 day -> 1 Yr)
- Fast Snapshot Restore (FSR): Full init of snapshot restoration without latency on the 1st time, cost $