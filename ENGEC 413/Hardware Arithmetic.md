The old multiplier needed n by n multiplications which leads to a latency of 4n. A better multiplication involves a 2n register that gets its upper half added two by a fixed n-register multiplicand (nx2n).

To make it even faster, take a look at the old shits. There are n partial products, so what if you just do all of them in one go? Sequentially, we held everything in an a register and accumulator which would give us $4n^2+1$ latency with a $2n$ bit RCA. "Un-rolling" the loop gets you A x B being a bunch of adders in a chain, but the longest route is $2n+2*2(n-2)+1=6n-7$.

We can do better if we move the adders in the last column to the bottom row and move around the wires, then you delay the addition carry forever. When you postpone the carry to the next column, the longest route is $2(n-1)+2(n-1)+1=4n-3$

### Floating Point from IEEE
Floating point numbers are hard to calculate. Sign (1), fraction (23) and exponent (8). The exponent is biased by a minus 127.