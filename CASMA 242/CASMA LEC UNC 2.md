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