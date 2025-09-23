# Homework 3
## 3.1. Sound Waves vs de Broglie Waves

a.i. T = 0.2 s
> $\omega=\frac{2\pi\text{ rad}}{T}=10\pi\text{ rad/s}$

a.ii. $\lambda=14\text{ m}$

a.iii. $v=\lambda/T=14/0.2=70 \text{ m/s}$

a.iv. Not enough information.

b.i. $\lambda=7*2=14\text{ nm}$

## 3.2. Commutators and Operators

a. Hadamard's Operator Lemma: $e^ABe^{-A}$
> $=(1+A+\frac{1}{2}A^2+\dots)B(1-A+\frac{1}{2}A^2+\dots)$
> $=(1+A+\frac{1}{2}A^2+\dots)B(1-A+\frac{1}{2}A^2+\dots)$
> $=(B+AB+\frac{1}{2}A^2B+\dots)(1-A+\frac{1}{2}A^2+\dots)$
> $=(B-BA+\frac{1}{2}BA^2+\dots)+(AB-ABA+\frac{1}{2}ABA^2+\dots)+\frac{1}{2}(A^2B-A^2BA+\frac{1}{2}A^2BA^2+\dots)$
> $=\Sigma_n\Sigma_m\frac{1}{n!m!}(-1)^{m}A^nBA^m$

What if we wanted to write the sum in terms of the $h=m+n$ and $m$? We still hit every one.
> $=\Sigma_h\Sigma_m^h\frac{1}{(h-m)!m!}(-1)^{m}A^{(h-m)}BA^m$

Let's address the super-commutator:
> $[A,B]=AB-BA$
> $[A,AB-BA]=AAB-ABA-ABA+BAA$

In other words, a "super-commutator" produces all "positions" that represent placing As around a B, with total "A"s being the commutators taken. In a commutator, the part that puts the "A" on the right (physically) side of B is negative, so it makes sense that an odd number of A's to the right of B would result in a negative term: (duplicates are counted courtesy of Pascal's Triangle a.k.a. combinatorial)
> $[A,[A,\cdots]]=\Sigma_{m=0}^n(-1)^m\frac{n!}{m!(n-m)!}A^{n-m}BA^{m}$

You'll realize that this format closely resembles the grouping of different "degrees" of terms from the exponential side of the problem. Because they are the same.
> $=\Sigma_{h=0}\Sigma_{m=0}^h(-1)^m\frac{1}{m!(h-m)!}A^{h-m}BA^{m}$
> $=\Sigma_{h=0}\frac{1}{h!}\Sigma_{m=0}^h(-1)^m\frac{h!}{m!(h-m)!}A^{h-m}BA^{m}$
> $=\Sigma_{h=0}\frac{1}{h!}[A,A[\dots]]$

b. $[\hat A,\hat B]f'(\hat B)$
> $\to f(\hat B)=f(0)+\hat Bf'(0)+\frac{1}{2}\hat B^2f''(0)+\dots=\Sigma\frac{1}{n!}\hat B^nf^{(n)}(0)$
> $\to f'(\hat B)=\hat f'(0)+\hat Bf''(0)+\dots=\Sigma\frac{1}{n!}\hat B^nf^{(n+1)}(0)$
> $\to [\hat A,\hat B]\Sigma\frac{1}{n!}\hat B^nf^{(n+1)}(0)$
> $=\hat A\hat B\Sigma\frac{1}{n!}\hat B^nf^{(n+1)}(0)-\hat B\hat A\Sigma\frac{1}{n!}\hat B^nf^{(n+1)}(0)$
> $=\hat A(f(0)-f(0)+\Sigma_{n=0}\frac{n+1}{(n+1)!}\hat B^{n+1}f^{(n+1)}(0))-\hat B\hat A\Sigma\frac{1}{n!}\hat B^nf^{(n)}(0)$
> $=\hat A(\Sigma_{n=0}\frac{n}{(n)!}\hat B^{n}f^{(n)}(0)-f(0))-\hat B\hat A\Sigma\frac{1}{n!}\hat B^nf^{(n)}(0)$
> $=\hat A(\Sigma_{n=0}\frac{n}{(n)!}\hat B^{n}f^{(n)}(0)-f(0))-\hat B\hat A\Sigma\frac{1}{n!}\hat B^nf^{(n)}(0)$

## 3.3. Eigen Eigen Eigen

Given:
> $H=\begin{pmatrix}\epsilon_0&\gamma e^{-i\chi}\\\gamma e^{+i\chi}&\epsilon_1\end{pmatrix}$

a. Find eigenvalues $\epsilon_g$ and $\epsilon_e$
> $\det (H-\lambda I)=0$
> $=\epsilon_0\epsilon_1-\lambda(\epsilon_0+\epsilon_1)+\lambda^2-\gamma^2$
> $=\lambda^2-\lambda(\epsilon_0+\epsilon_1)+\epsilon_0\epsilon_1-\gamma^2$
> $\to\lambda=(\epsilon_0+\epsilon_1\pm\sqrt{\epsilon_0^2+2\epsilon_0\epsilon_1+\epsilon_1^2-4\epsilon_0\epsilon_1+4\gamma^2})/2$
> $=(\epsilon_0+\epsilon_1\pm\sqrt{\epsilon_0^2-2\epsilon_0\epsilon_1+\epsilon_1^2+4\gamma^2})/2$
> $=(\epsilon_0+\epsilon_1\pm\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})/2$
> $\epsilon_g=(\epsilon_0+\epsilon_1+\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})/2$
> $\epsilon_e=(\epsilon_0+\epsilon_1-\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})/2$

b. Find their respective eigenvectors $\ket{\psi_g}$ and $\ket{\psi_e}$
> $0=(\epsilon_0-\epsilon_1+\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})v_1/2+\gamma e^{-i\chi}v_2$
## 3.4. Heisenberg is Uncertain


## 3.5. Harmony and Superposition

