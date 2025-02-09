- Ingress Traffic (into/inside the AWS network) is typically free
- Egress traffic is costly (from aws network to the internet) 

Rule of thumb: try to minimize the Egress traffic, use services can cost more money but in some scenarios can help keep network cost low (EG: Accessing S3 bucket through the public internet with NATGW & InternetGW and using VPC Endpoint).