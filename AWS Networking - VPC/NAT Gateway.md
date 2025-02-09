![[nat-gateway-vs-instance.png]]
NAT Gateway is recommended instead of NAT Instance

Traffic flow:  from priv subnet > NAT Gateway > Internet Gateway > Internet

Bandwidth from 5Gbps 

Must edit the route table of the private subnet to point to the NAT Gateway