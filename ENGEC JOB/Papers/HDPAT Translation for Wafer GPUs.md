![[Pasted image 20260203144401.png]]
A Wafer-scale GPU connects many chiplets in a quality (high bandwidth, low latency) network which seeks to beat multi-GPU setups. Scaling creates new bottle necks with virtual to physical addresses being smothered. HDPAT (hardware-accelerated distributed page address translation) addresses this challenge through:
1. **Concentric caching**: Inner layer GPMs serve as translation providers for outer layer GPMs, reducing path length. Rotation guarantees a small number of hops.
2. **Redirection table**: IOMMU can now distribute page table walk workloads to GPMs, whose caches help out other GPMs, thereby reducing latency. 
3. **Proactive prefetching**: GPMs are told to cache potentially needed addresses before they are explicitly searched for. 
## Background
Here are some help terms:
1. Wafer-Scale GPU Architecture: Each GPU Processing module (GPM) functions as an independent GPU with multiple compute units and DRAM. All GPMs get abstracted away to one single wafer-scale GPU. Requesting pages gets distributed contiguously among the GPMs, which minimizes memory access overhead.
2. Address Translation: When a CU requires address translation, it traverses a few layers with page table (PT) walkers.
3. TLB Sharing:
4. IO Memory Management Unit (IOMMU): Conventional units handle 1-4 GPUs adequately. HDPAT distributes the unit's translation workload to wafer-scale GPMs.