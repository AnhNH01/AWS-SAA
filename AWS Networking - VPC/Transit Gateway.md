
**Note**: The **only** service that support multicast

Network topologies can be complex, especially with multiple peered VPC, because [[VPC Peering]] is not transitive

![[transit-gw-complex-networkk-topo.png]]

AWS provide transit gateway as a transitive peering between VPCs, and onprems, like a star model (everything connects to the transit gateway and it will work)

![[vpc-transitive-peering.png]]

Other use cases:
- Site to site VPN Equal Cost Multi-path Routing (increase through put)
![[increased-bandwidth-ECMR.png]]

- Sharing Direct connect connection between multiple accounts