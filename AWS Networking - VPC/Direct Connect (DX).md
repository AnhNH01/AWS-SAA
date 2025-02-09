
Direct connect is a way for you to create a **private connection** from on prem to your vpcs and other aws resources (**without traffic on the public internet**).

You have to request to AWS, and the lead time can be more than **1 month**.

Requests is made to AWS first, and then completed by AWS direct connect partners

- Dedicated Connection: 1 GBbs -> 10 Gbps -> 100 Gbps
	-> Physical ethernet port on server

- Hosted Connection: 50Mbps, 500Mbps, to 10Gbps
	-> Add or remove bandwidth on demand
	-> 1, 2, 5, 10 Gbps available at selected AWS direct connect partners

Traffic through DX is **NOT encrypted**, but private. If you want encrypted traffic, add vpn to provide IP-sec encrypted traffic

![[DX-ipsec-encrypted-traffic.png]]

**Resiliency** for critical workloads

- High -> 1 connection, multiple Direct Connect locations
- Maximum -> Multiple connection, multiple Direct Connect locations.

**Usecase for DX**
- High throughput for data intensive applications

**Back up**
- You can set up [[Site to Site VPN]] as backup for your connection for the unlikely event that Direct connect location fails.