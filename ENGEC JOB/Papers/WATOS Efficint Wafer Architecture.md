Wafer blah blah, WATOS is a co-exploration framework for LLM training strategy and wafer architecture.
- define a hardware template to explore arch parameters
- capitalize on high D2D bandwidth and other advantages
### Training
Batching is adopted to improve communication efficiency and accelerate convergence, but take a lot of memory, ill suited to WSCs. However, activation recomputation is much better for WSCs as it doesn't transfer any data.

Prevent