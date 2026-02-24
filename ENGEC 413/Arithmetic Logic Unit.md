### Combinational Logic
The critical path is the path with the longest delay. If we want to reduce the overall latency of the system, then we want to get shorten the critical path.
### Sequential Circuits
The latency is added up among all the consecutive combinational logic and the **clock period** is determined by the largest latency. Count the largest cycle pipeline and multiply it by the clock period to get the total latency.

Because the ripple carry adder takes too many clock cycles (2n), we can split up the MSB and LSB into two separate adders. The MSB is computed twice expecting both the carry in and no carry in and the carry out of the LSB adder selects which prediction should be chosen for the final result. 

Overflow occurs when you try to store a value not intended to fit inside a cell size. In twos complement, 