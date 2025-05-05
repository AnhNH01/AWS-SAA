Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=187|AWS Certified Solutions Architect Slides v40, page 187]]

Managed in-memory caches services (Redis, Memcahed)

Using ElasticCache require heavy application code change (because you might need to add additional caching logic if it hadn't exist in your codebase).



**Security**
- Enable IAM authentication for Redis 
- IAM polices are applied for API Level
- Memcached support SASL-based Authentication 

Note:
- Utilize Redis sorted set to implement gaming leaderboard
- You can store session data of user into elasticache
