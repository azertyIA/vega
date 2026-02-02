Moore's Law and AI makes IEEE 754 really bad. It wastes money. Posit has a way to compute with real numbers. Has the potential to use less bits. etc. 

### Game of Twenty Questions
The idea behind information theory is that you should be able to discern an idea with a limited amount of bits. Typical binary integers answer this by reading an integer by subdividing the domain by half. But real numbers are MUCH harder to get around. Computers only have so much memory is apparently a fallacy when applied to floats

### Representing the Reals
All the reals can be easily represented with just three bits:
```
000 - 0
001 - (0,1)
010 - 1
011 - (1,F)
100 - NAR
101 - (-F,-1)
110 - -1
111 - (-1,0)
```

Reciprocation and negatives are very cool to implement. Just do a quick little algorithm. To make your numbers, just answer some questions and assume that there are infinitely many zeros. 
$$x=((1-3S)+F)\times2^{z}$$
$$z=(-1)^S\times(r+S)$$
Parallelization destroys associativity which floats don't really like. 32-bits (float) usually isn't enough. People use doubles all the time. I'm not following his justification for getting rid of $\pm0$. More parallelizing issues. 
### 11 Design Principals for a Number System
1. The distribution should resemble the needed numbers
2. No redundant bits
3. No hidden modes of operation. Should be deterministic.
4. All operations should be correctly rounded.
5. Should be easy to change precisions.
6. Errors should propagate to the final output.
7. Should be fast to build in software.
8. Scalable to any number of bits.
9. Real numbers should be ordered like integers.
10. Negating a real should be negated like an integer.
11. Mimics infinite precision.
### Application
There's a whole stack for posits. It's very cool. For 32-bit floats you get a dynamic range of 83 decades that's consistent everywhere. Meanwhile, posits have a more triangular thing going on. 
### Solving Associativity
Every n-bit posit environment has a $16n$-bit fixed-point accumulator. Exact dot product are guaranteed up to 2 billion-long vectors. People usually use double precision for accumulation. Strassen matrix multiplication is both faster and numerically safer. It's a vector of 16 integers. Posits do better than floats in classification. Posits allow for customization on its accuracy.
### Breakthrough: the b-posit
It's apparently good for decode encode time, but I don't know how b-posits work...
