When you need ssh connection to ec2 in private subnet, ssh to an ec2 in public subnet (bastion host), and then from bastion host ssh to the ec2s in the private subnet.
![[Bastion Host.png]]

You can access the ec2 in the private subnet, but the ec2 in the private subnet still does not have internet connection, and to resolve that, we need NAT

**[[Nat Instance]]**(**out dated**, but still in exam), **[[NAT Gateway]]**