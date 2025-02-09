**Intuition:** *Think of it like a network USB disk.*

EBS is AZ bound.

**Note**: Delete on termination -> control the behavior of EBS when the EC2 instance it is attached to is terminated. 
- For **root** volume -> Default **enable**
- For other volume -> Default **disable**