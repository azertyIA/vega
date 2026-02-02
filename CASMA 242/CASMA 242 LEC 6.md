## Standard Matrix

You can make a matrix by looking at how the transformation outputs given basis vectors as inputs, which makes everything really simple:

> $T(e_n)=c_n$
> $A=\begin{pmatrix}c1&\dots&c_n\end{pmatrix}$

We can add matrices. Slot by slot. Duh.

$A$ has an inverse matrix is defined by a $C$ where $AC=CA=I_n$

Composition works as follows for inverses $T$ and $S$:
> $S(T(x))=x$
> $T(S(x))=x$

_Theorem:_ A linear transformation is invertible if and only if the standard matrix is invertible of $T^{-1}$ is $A^{-1}$.

Time for Matrix factorization:

Given an upper triangular matrix:
```
[ 1 2 3 
  0 1 2
  0 0 1 ]
```

This is a really easy matrix to find solutions for. A lower triangular is also easy:
```
[ 1 0 0 
  1 2 0
  1 2 3 ]
```

```
[ 0 1    [ 2 4   [ 2  4
  2 3 ]    2 3 ]   0 -1 ]
```

Assume that $A$ is an $m\times n$ matrix that can be reduced to echelon form without swapping rows:
> $A=LU$
> where $L$ is an $m\times m$ matrix that is lower triangular with 1's in the diagonal.
> where $U$ is an $m\times n$ matrix in the echelon form of $A$

When given an $Ax=v$,
> $v=Ax=L(Ux)=Ly$

We can achieve this by reducing $A$ to some echelon form by a sequence of row replacement operations, if possible. Place entries in L such that the same sequence of row operations reduces L to I. $U$ is just the echelon form.