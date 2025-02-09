- Makes the VPCs acts as if they are in the same network (connected using AWS network)

- Peered accross regions, accoutns

- Must edit all route table of subnets, vpc to allow traffic

- **NOT transitive**, which means we have to peer every pair (A p B),  (B p C) still require (A p C)