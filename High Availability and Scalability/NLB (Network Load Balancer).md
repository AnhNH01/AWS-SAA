Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=139|AWS Certified Solutions Architect Slides v40, page 139]]

- Operate on L4 (Transport Layer): Forward TCP and UDP traffic to target group
- Hyper-performant
- **Not** in free tier

Network Load Balancer has one static IP per AZ, useful if you want to expose your application on only a set of IP (example on some whitelisted ips).