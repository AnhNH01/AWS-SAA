Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=152|AWS Certified Solutions Architect Slides v40, page 152]]

Naming:
CLB: Connection Draning
ALB, NLB: Deregistration delay

-> Time to wait for the in-flight requests to be completed while the intance is being marked unhealthy and the LB stops sending traffic to it.

Range from 0(disabled) to 3600: set lower if requests are short.