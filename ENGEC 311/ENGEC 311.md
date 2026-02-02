## Carry Lookahead Adder

C1 could be 1 if A0 and B0 (generate) are both 1 obviously, but it could also be a one if (A0 xor B0) and C0 (propagate) is 1. (From the full adder).
> $C_{n+1}=A_nB_n+(A_n\oplus B_n)C_n$
> $=G_n+P_nC_n$

Let's see how complex going up to 2 is.
> $C_1=G_0+P_0C_0$
> $C_2=G_1+P_1(G_0+P_0C_0)$
> $=G_1+P_1(G_0+P_0C_0)$
> $=G_1+P_1G_0+P_1P_0C_0$
> $C_2=G_2+P_2(G_1+P_1G_0+P_1P_0C_0)$
> $=G_2+P_2G_1+P_2P_1G_0+P_2P_1P_0C_0$

