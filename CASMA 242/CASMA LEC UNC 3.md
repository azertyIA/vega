In applications of linear algebra, vector spaces appear as
1. The set of all solutions to a linear system oy homogeneous linear equations
2. The set of linear combinations of vectors

We say that the set $x$ that satisfied the system gave us the solution set of the system. We will call the set of x that satisfies $Ax=0$ the *null space* of matrix $A$, indicated as $\text{Nul}(A)$. 

```
Given [ 1 -3 -2 ;
	   -5  9  1 ]
	   
u = [ 5; 3; -2 ]

Au = [ 0; 0 ] // u in Nul(A) (vector space)
```

Three conditions to a subspace:
1. Is $\vec0$ in there?
2. Is addition complete?
3. Is multiplication complete?

```
R4 (a,b,c,d) that satisfy
- a-2b+5c-d=0
- -a-b+c=0

[ 1 -2  5 -1 ;
 -1 -1  1  0 ]

for h in H: Ah = 0
```

$\text{Col}(A)$ corresponds to the span of the columns of $A$ or its *column space*. It is the biggest when $A$ is onto. If $A$ is one-to-one, then the null space is the smallest.

An indexed set of vectors $\{v_1,\dots,v_n\}$ is said to be linearly independent if the linear combination is zero only when all the coefficients are zero.  This can apply to polynomials as well.

Change of basis.
```
[b1 b2]_C [x]_B = [X_C]
P_{C <- B} [x]_B = [X_C]
P_{C <- B}^{-1} = P_{B <- C}-

P_{E <- B} [x]_B = [x]_E = x
[B] [x_B] = x
[x_B] = [B]^-1 x

P_{CB} = P_{CE} P_{EB}
P_{CB} = P_{EC}^-1 P_{EB}
P_{CB}  = [C]^-1 [B]

for quickness: (Aa = I)
[A | B] ~ a[A | B] = [I | aB] 
```

Polynomials.
```
B = {1+t+t2, 1+t, t+t2}
C = {1, 1+t2, t2}

		 / 1  1  1 \
P_{CB} = | 1  1  0 |
		 \ 0 -1  1 /
```

