Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=166|AWS Certified Solutions Architect Slides v40, page 166]]

Read replica network cost:
-> Usually when data transfer across AZ, they will incur a cost, for read replicas, if they are in the same region, no cross AZ network cost


**RDS MultiAZ (Disaster Recovery)**
Differ from read replicas that is sync every operation from your master database to your slave database (*Synchronous replication*). You will be provided with a *single DNS name that your application communicates with*. Provide automatic failover


-> Using RDS multi AZ will not require connection string change in your application.