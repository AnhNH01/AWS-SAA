Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=146|AWS Certified Solutions Architect Slides v40, page 146]]

Cross-Zone Load Balancing: Distribute traffic across all registered instance in all AZs

Without: Distribute across LB nodes


ALB: on by default, turn off at target group level, no inter AZ costs

GWLB, NLB: off by default, incur inter AZ costs

CLB: off by default, no inter AZ costs

