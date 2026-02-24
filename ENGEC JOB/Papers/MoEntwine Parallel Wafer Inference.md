![[Pasted image 20260203154154.png]]
Mixture of experts has become a common technology in SOTA models. It relies on parallelism (among different experts) to alleviate memory bottleneck. However, GPU to GPU communication isn't adequate enough for scale making wafer-scale chips a better option as a networking device, not without its own issues.

![[Pasted image 20260203154233.png]]
Entwined Ring Mapping co-designs the mapping of attention and MoE layers to balance communication and achieve better overall performance. The Non-invasive balancer splits a complete expert into multiple steps and alternately uses the cold links of both layers.