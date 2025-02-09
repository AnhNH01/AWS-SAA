VPC enpoints provide a way so ec2 instances in private network can access AWS services in the internet without traffic going through NATGW and IGW (which costs money)

There are **2 types** of VPC Enpoints
- Interface (powered by PrivateLink)
	-> Provide ENI, must use security group
	-> Cost money $hourly + $ per GB of data processed
	-> Support most services

![[vpc-enpoint-interface.png]]

- Gateway
	-> Free
	-> Support S3, DynamoDB
	-> Must be the target in a route table
	-> Scale horizontally

![[vpc-endpoint-gateway.png]]

**Note**
- For s3 and dynamo db, most likey prefer Gateway (because its free)
- Use interface for advanced use case like access from onprem (Site to Site VPN, Direct Connect), a different VPC or different region

![[vpc-enpoint-interface-vs-gateway.png]]