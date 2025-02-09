![[nat-instance-overview.png]]

This is the instance that provide NAT for the ec2 in the private subnet,
- Must be attached to an EIP
- Turn off source/destination check (because of the addr rewrites)