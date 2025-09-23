# Solutions Set of Linear Systems

Let's start today off with a matrix and a vector:
> $\begin{pmatrix}3&5&-4&7\\-3&-2&4&-1\\6&1&-8&-4\end{pmatrix}$
> $\begin{pmatrix}3&5&-4&7\\0&3&0&6\\6&1&-8&-4\end{pmatrix}$
> $\begin{pmatrix}3&5&-4&7\\0&3&0&6\\0&-9&0&-18\end{pmatrix}$
> $\begin{pmatrix}3&5&-4&7\\0&1&0&2\\0&0&0&0\end{pmatrix}$
> $\begin{pmatrix}3&0&-4&-3\\0&1&0&2\\0&0&0&0\end{pmatrix}$
> $\begin{pmatrix}1&0&-4/3&-1\\0&1&0&2\\0&0&0&0\end{pmatrix}$

> $x_2=2$
> $x_1=-1+4x_3/3$
> $[-1+4x_3/3,2,x_3]=x_3[4/3,0,1]+[-1,2,0]$

A solution set of a linear system has only one unique solution when there is only a pivot in every column, making every variable a *basic variable*.

A set of vectors in $\mathbb{R}^n$ are linearly independent if $\Sigma xv=0$ has just the trivial solution.

For example, $v_1=[0,0,2],v_2=[0,1,2],v_3=[1,2,3]$. If you put it into a augmented matrix and solve for it you'll find you end up with three pivots for every column, thereby making everything linear independent.

Determine if the columns are linearly independent:
> $\begin{pmatrix}0&1&4&0\\1&2&-1&0\\5&8&0&0\end{pmatrix}$
> $\begin{pmatrix}1&2&-1&0\\0&1&4&0\\5&8&0&0\end{pmatrix}$
> $\begin{pmatrix}1&2&-1&0\\0&1&4&0\\0&-2&5&0\end{pmatrix}$
> $\begin{pmatrix}1&0&4&0\\0&1&4&0\\0&0&13&0\end{pmatrix}$
> $\begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&1&0\end{pmatrix}$

Given the following matrix (3x4), note the third column is the sum of the other two, find a non-trivial solution. (1, 1, -1), so it's not linearly independent.

The only way a vector could be linearly dependent is if the vector is 0. For two vectors to be linear dependent, you need to be able to multiply a factor by one to get the other. For more, they just need to add to 0.

Given two linearly independent vectors, if a vector $w$ is in the span of those two vectors, then $w$ in combination with the vectors make a linearly dependent set. If there are more vectors than columns, then the set is linearly dependent.