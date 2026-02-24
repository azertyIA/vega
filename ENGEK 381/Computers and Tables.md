There used to be people who worked as computers back then who usually refers to tables to get their values. For example logarithms and sines used to be a huge ass lookup table. Babbage wanted to make the mechanic analytic engine, but the machining was never there for his lifespan

Ada Lovelace came up of a better way of doing calculations via programming and algorithms. The gap in education nowadays is that we're stuck in a world with NN and finding minimums rather than sines and cosines back then. 

Okay so now there's some function for a Gaussian CDF:
$$\Phi(z)=\int_{-\infty}^zdw$$
$$F_X(w)=\Phi(\frac{w-\mu}{\sigma})$$
$$(\mathbb E,var)[aX+b]=(a\mu+b,a^2\sigma^2)$$
$$X=\text{Gauss}(\mu,\sigma^2)$$
For example, given $\text{Gauss}(3,2)$:
1. $P[x<3]=\frac12$ (symmetry)
2. $P[x\geq0]=1-P[x<0]$
	- $=1-F_X(0)$
	- $=1-\Phi(\frac{0-3}{\sqrt2})$
3. $P[x\geq0|x<3]=\frac{P[0<x<3]}{P[x<3]}$
	- $=(\Phi(0)-\Phi(-3/\sqrt2))/0.5$
	- $=(0.5-\Phi(-3/\sqrt2))/0.5$
	- $=1-2\Phi(-3/\sqrt2)$
4. $\mathbb E[-2X+1]=-2\mathbb E[X]+1$
5. $Var[-2X+1]=(-2)^2*Var[X]$

For $\text{Exponential(4)}$:
1. $\mathbb E[X^2]=Var[X]+E[X]^2$
	- $1/16+1/16$
	- $1/8$
	