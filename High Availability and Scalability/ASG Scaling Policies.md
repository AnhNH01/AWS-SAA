Slide: [[AWS Certified Solutions Architect Slides v40.pdf#page=158|AWS Certified Solutions Architect Slides v40, page 158]]


- Dynamic Scaling
	- Simple scaling: perform action when an CW alarm is triggered
	- Step scaling: setup multiple thresholds for scale
	- Target tracking: auto scale to maintain a metric at around targeted value
- Schedule Scaling: if you know the traffic pattern

- Predictive Scaling: apply machine learning to predict future load

- Scaling cooldown: cooldown for some time if the threshold for scaling is crossed, the idea is wait for the metrics to stabilize.