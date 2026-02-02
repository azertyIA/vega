## 9.1. Squeezed states
Given the equations of motion for the Harmonic Oscillator:
> $i\hbar\partial_t\hat x(t)=[\hat x(t),\hat H(\hat x,t)]$
> $i\hbar\partial_t\hat p(t)=[\hat p(t),\hat H(\hat x,t)]$
> $i\hbar=[\hat x(t),\hat p(t)]$

Given Hamiltonian mechanics, we know that $-\partial_t\hat p(t)=\partial_x\hat H$ and $\partial_t\hat x(t)=\partial_p\hat H$.
> $\hat H=\hat p^2/2m+m\omega^2\hat x^2/2$
> $-\partial_t\hat p=\partial_\hat x\hat H=m\omega^2\hat x$
> $\partial_t\hat x=\partial_\hat p\hat H=\hat p/m$
> $\partial_t^2\hat x=-\omega^2\hat x$
> $\hat x(t)\ket\psi=A\cos(\omega t)+B\sin(\omega t)$
> $\hat x(0)\ket\psi=A+0$
> $\hat x(t)=\hat x(0)\cos(\omega t)+B\sin(\omega t)$
> $\hat p(t)=\hat p(0)\cos(\omega t)+B\sin(\omega t)$

> $\partial_t\hat x(t)|_{t=0}=0+\omega B\cos(0)=\hat p(0)/m=\partial_\hat p\hat H|_{t=0}$
> $B=\hat p(0)/m\omega$
> $\boxed{\hat x(t)=\hat x(0)\cos(\omega t)+\frac1{m\omega}\hat p(0)\sin(\omega t)}$

> $-\partial_t\hat p(t)|_{t=0}=0-\omega B\cos(0)=m\omega^2\hat x(0)=\partial_\hat x\hat H|_{t=0}$
> $B=m\omega\hat x(0)$
> $\boxed{\hat p(t)=\hat p(0)\cos(\omega t)+m\omega\hat x\sin(\omega t)}$

b.i. Given $\ket\Phi=\frac{\sqrt3}2\ket0+\frac12\ket1$ and $\hat x=\Delta_x(\hat a^\dagger+\hat a)$
> $\sqrt{\braket{\Phi|\hat x^2|\Phi}-\braket{\Phi|\hat x|\Phi}^2}$
> $=\Delta_x\sqrt{\braket{\Phi|(\hat a^\dagger + \hat a)^2|\Phi}-\braket{\Phi|\hat a^\dagger + \hat a|\Phi}^2}$
> $=\Delta_x\sqrt{\braket{\Phi|\hat a^{\dagger2}+\hat a\hat a^\dagger+\hat a^\dagger\hat a+\hat a^2|\Phi}-\braket{\Phi|\hat a^\dagger + \hat a|\Phi}^2}$
> $=\Delta_x\sqrt{\braket{\Phi|\hat a\hat a^\dagger+\hat a^\dagger\hat a|\Phi}-\braket{\Phi|\hat a^\dagger + \hat a|\Phi}^2}$
> $=\Delta_x\sqrt{\braket{\Phi|2\hat N+1|\Phi}-(\braket{\Phi|\hat a^\dagger|\Phi} + \braket{\Phi|\hat a|\Phi})^2}$
> $=\Delta_x\sqrt{\braket{\Phi|2\hat N|\Phi}+1-\frac3{16}(\braket{1|\hat a^\dagger|0}+\braket{0|\hat a|1})^2}$
> $=\Delta_x\sqrt{\braket{\Phi|2\hat N|\Phi}+1-\frac3{16}(\braket{1|1} + \braket{0|0})^2}$
> $=\Delta_x\sqrt{\braket{\Phi|2\hat N|\Phi}+1-\frac34}$
> $=\Delta_x\sqrt{\braket{\Phi|2\hat N|\Phi}+\frac14}$
> $=\Delta_x\sqrt{\frac14\braket{1|2\hat N|1}+\frac14}$
> $=\Delta_x\sqrt{\frac12+\frac14}$
> $=\boxed{\Delta_x\sqrt{3}/2}$, smaller than $\Delta_x$, so a squeeze state

b.ii. Given $\ket\Phi=\frac{\sqrt3}2\ket0+\frac12\ket1$ and $\hat p=i\Delta_p(\hat a^\dagger-\hat a)$
> $\sqrt{\braket{\Phi|\hat p^2|\Phi}-\braket{\Phi|\hat p|\Phi}^2}$
> $=\Delta_p\sqrt{-\braket{\Phi|(\hat a^\dagger - \hat a)^2|\Phi}+\braket{\Phi|\hat a^\dagger - \hat a|\Phi}^2}$
> $=\Delta_p\sqrt{\braket{\Phi|1+2\hat N|\Phi}+(\braket{\Phi|\hat a^\dagger|\Phi} - \braket{\Phi|\hat a|\Phi})^2}$
> $=\Delta_p\sqrt{1+2\braket{\Phi|\hat N|\Phi}+\frac3{16}(\braket{1|\hat a^\dagger|0} - \braket{0|\hat a|1})^2}$
> $=\Delta_p\sqrt{1+\frac12+\frac3{16}(\braket{1|\hat a^\dagger|0} - \braket{0|\hat a|1})^2}$
> $=\Delta_p\sqrt{1+\frac12+\frac3{16}(\braket{1|\hat a^\dagger|0} - \braket{0|\hat a|1})^2}$
> $=\Delta_p\sqrt{1+\frac12}$
> $=\boxed{\Delta_p\sqrt{3/2}}$

The product is thus $\Delta_x\Delta_p(3/\sqrt8)$ which is bigger than the ground state uncertainty ($\Delta_x\Delta_p$). So, just because it's a squeeze state, doesn't mean the actual uncertainty gets violated.
## 9.2. Coherent States
> $\hat x=\Delta_x(\hat a^\dagger+\hat a)$
> $\hat p=i\Delta_p(\hat a^\dagger-\hat a)$
> $\hat a\ket\alpha=\alpha\ket\alpha$
> $\bra\alpha\hat a^\dagger=\bra\alpha\alpha^*$

> $\braket{\alpha|\hat x|\alpha}=\Delta_x\braket{\alpha|\hat a^\dagger+\hat a|\alpha}$
> $=\Delta_x(\braket{\alpha|\hat a^\dagger|\alpha}+\braket{\alpha|\hat a|\alpha})$
> $=\Delta_x(\braket{\alpha|\alpha^*|\alpha}+\braket{\alpha|\alpha|\alpha})$
> $=\Delta_x(\alpha^*+\alpha)$
> $=\Delta_x2\Re\alpha$
> $\braket{\hat X}=2\Re\alpha$

> $\braket{\alpha|\hat p|\alpha}=i\Delta_p\braket{\alpha|\hat a^\dagger-\hat a|\alpha}$
> $=i\Delta_p(\braket{\alpha|\hat a^\dagger|\alpha}-\braket{\alpha|\hat a|\alpha})$
> $=i\Delta_p(\braket{\alpha|\alpha^*|\alpha}-\braket{\alpha|\alpha|\alpha})$
> $=i\Delta_p(\alpha^*-\alpha)$
> $=\Delta_p2\Im\alpha$
> $\braket{\hat P}=2\Im\alpha$

$\braket{\alpha|\hat X^2|\alpha}=\braket{\alpha|(\hat a+\hat a^\dagger)^2|\alpha}$
> $=\braket{\alpha|\hat a\hat a+\hat a\hat a^\dagger+\hat a^\dagger\hat a+\hat a^\dagger\hat a^\dagger|\alpha}$
> $=\braket{\alpha|\alpha^2+(2\hat N+1)+\alpha^\dagger|\alpha}$
> $=\braket{\alpha|\alpha^2+(2|\alpha|^2+1)+\alpha^{*2}|\alpha}$
> $=\alpha^2+2|\alpha|^2+1+\alpha^{*2}$

$\Delta_X=\sqrt{\braket{\hat X^2}-\braket{\hat X}^2}$
> $=\sqrt{\alpha^2+\alpha^{*2}+2|\alpha|^2+1-\alpha^2-\alpha^{*2}-2|\alpha|^2}$
> $=\sqrt{1}=1$

$\braket{\alpha|\hat P^2|\alpha}=-\braket{\alpha|(\hat a-\hat a^\dagger)^2|\alpha}$
> $=-\braket{\alpha|\hat a\hat a-\hat a\hat a^\dagger-\hat a^\dagger\hat a+\hat a^\dagger\hat a^\dagger|\alpha}$
> $=-\braket{\alpha|\alpha^2-(2\hat N+1)+\alpha^\dagger|\alpha}$
> $=-\braket{\alpha|\alpha^2-(2|\alpha|^2+1)+\alpha^{*2}|\alpha}$

$\Delta_P=\sqrt{\braket{\hat P^2}-\braket{\hat P}^2}$
> $=\sqrt{-(\alpha^2+\alpha^{*2}-2|\alpha|^2-1)+(\alpha^2+\alpha^{*2}-2|\alpha|^2})$
> $=\sqrt{1}=1$

Thus the uncertainty is the same as achieved in the ground state: $\boxed{\Delta_X\Delta_P=1}$
## 9.3. Operator Identities
Given:
> $[\hat A,[\hat A,\hat B]]=0$
> $[\hat B,[\hat A,\hat B]]=0$
> $e^{\hat A+\hat B}=e^\hat Ae^\hat Be^{-\frac12[\hat A,\hat B]}$

If $\hat C=[\hat A,\hat B]$, then the following is also true:
> $[\hat A,\lambda\hat C]=0$
> $[\hat B,\lambda\hat C]=0$
> $[\hat A+\hat B,\lambda\hat C]=0$

And more interestingly:
> $[\hat A+\hat B,[\hat A+\hat B,\lambda\hat C]]=0$
> $[\lambda\hat C,[\hat A+\hat B,\lambda\hat C]]=0$

Setting $\hat A+\hat B=\hat M$ and $\lambda\hat C=\hat N$:
> $[\hat M,\hat N]=0$
> $[\hat M,[\hat M,\hat N]]=0$
> $[\hat N,[\hat M,\hat N]]=0$
> so $e^{\hat M+\hat N}=e^\hat Me^\hat Ne^{-\frac12[\hat M,\hat N]}=e^\hat Me^\hat N$ given by the relation at the start

Substituting things back in in terms of $\hat A,\hat B$ and $\hat C$:
> $e^{\hat M+\hat N}=e^\hat Me^\hat N$
> $e^{\hat A+\hat B+\lambda\hat C}=(e^{\hat A+\hat B})e^{\lambda\hat C}$
> $=(e^{\hat A}e^{\hat B}e^{-\frac12[\hat A,\hat B]})e^{\lambda\hat C}$ (the first relation)

And in terms of just $\hat A$ and $\hat B$:
> $e^{\hat A+\hat B+\lambda[\hat A,\hat B]}=e^{\hat A}e^{\hat B}e^{-\frac12[\hat A,\hat B]}e^{\lambda[\hat A,\hat B]}$

Finally for $\lambda=\frac12$:
> $\boxed{e^{\hat A+\hat B+\frac12[\hat A,\hat B]}=e^{\hat A}e^{\hat B}}$

Checking for the case if $[\hat A,\hat B]=0$, and it works:
> $e^{\hat A+\hat B+0}=e^{\hat A+\hat B}=e^{\hat A}e^{\hat B}e^{-\frac12[\hat A,\hat B]}=e^{\hat A}e^{\hat B}e^0=e^{\hat A}e^{\hat B}$
## 9.4. Landau Levels

a. $\vec B=\nabla\times\vec A$
> $=\nabla\times\braket{-B_0y,0,0}$
> $=\boxed{\braket{0,0,B_0}}$

b. There is a box, where a periodic boundary is implied:
> $\psi(x,y)=\psi(x+nL_x,y+nL_y),n\in\mathbb Z$

Plugging in all that we can for the Hamiltonian:
> $E\braket{x|\psi}=\frac1{2m}(-i\hbar\nabla-q\vec A(\vec x))^2\braket{x|\psi}$
> $=\frac1{2m}(\braket{-i\hbar\partial_x,-i\hbar\partial_y,-i\hbar\partial_z}-\braket{-qB_0y,0,0})^2\braket{x|\psi}$
> $=\frac1{2m}(\braket{-i\hbar\partial_x+qB_0y,-i\hbar\partial_y,-i\hbar\partial_z})^2\braket{x|\psi}$
>$=\frac1{2m}((-i\hbar\partial_x+qB_0y)^2-\hbar^2\partial_y^2)\braket{x|\psi}$ (z shouldn't matter or change)
>$=\frac1{2m}((-i\hbar\partial_x+qB_0y)^2-\hbar^2\partial_y^2)\braket{x|\psi}$
>$=\frac1{2m}(-\hbar^2\partial_x^2+2qB_0y(-i\hbar\partial_x)+(qB_0y)^2-\hbar^2\partial_y^2)\braket{x|\psi}$

Since the Hamiltonian has basically no x-dependence like y does, one can assume the wavefunction looks like:
> $\braket{\vec x|\psi}=e^{ik_xx}\phi(y)$
> $\braket{\vec x|\hat H|\psi}=\hat He^{ik_xx}\phi(y)$
> $=(e^{ik_xx})\frac1{2m}(\hbar^2k_x^2+2qB_0y(\hbar k_x)+(qB_0y)^2-\hbar^2\partial_y^2)\phi(y)$
> $=(e^{ik_xx})\frac1{2m}((\hbar k_x+qB_0y)^2-\hbar^2\partial_y^2)\phi(y)$
> $=(e^{ik_xx})(-\frac{\hbar^2\partial_y^2}{2m}+\frac{(\hbar k_x+qB_0y)^2}{2m})\phi(y)$
> $=(e^{ik_xx})(-\frac1{2m}(\hbar^2\partial_y^2)+\frac12(m(qB_0/m)^2)(y+\frac {\hbar k_x}{qB_0})^2)\phi(y)$
> $\hat H_{harmonic}=-\frac1{2m}\hbar^2\partial_x^2+\frac1{2}{m\omega^2}x^2$

That's basically a harmonic oscillator with a shifted origin. 
> The oscillator frequency is $|q|B_0/m$.
> The center is at $-\hbar k_x/qB_0$.

So regardless of a known $k_x$, you can get quantized energy eigenvalues:
> $\boxed{E_n=\hbar\omega(n+\frac12)=\frac{\hbar|q|B_0}m(n+\frac12)}$

Given the boundary conditions:
> $\psi(x,y)=e^{ik_xx}\phi(y)=e^{ik_x(x+L_x)}\phi(y)=\psi(x+L_x,y)$
> $1=e^{ik_x(L_x)}\to k_x=2\pi n/L_x$

The center however must be bounded in the square:
> $0\leq\frac\hbar{eB_0}2\pi n/L_x\leq L_y$
> $n\leq eB_0L_xL_y/2\pi\hbar=eB_0L_xL_y/h$

The associated degeneracy is thus:
> $\boxed{N=eB_0L_xL_y/h=B_0A/\Phi_0=\Phi/\Phi_0}$ (i forgot if I'm off by a factor of 2)

c. $\vec A=\braket{0,B_0x,0},\tilde A=\braket{-\frac12B_0y,\frac12B_0x,0}$
> $\tilde A=\vec A+\nabla\Lambda$
> $\braket{-\frac12B_0y,-\frac12B_0x,0}=\braket{\partial_x\Lambda,\partial_y\Lambda,\partial_z\Lambda}$
> $\partial_z\Lambda=0$
> $\partial_x\Lambda=-\frac12B_0y$
> $\partial_y\Lambda=-\frac12B_0x$
> $\boxed{\Lambda=-\frac12B_0x}$
## 9.5. Non-Relativistic Gauge Invariance

Given
> $\hat U=\exp[iq\Lambda(\vec x)/\hbar]=\exp[-ie\Lambda(\vec x)/\hbar]$
> $\ket{\tilde\Psi}=\hat U\ket\Psi$
> $\hat U^\dagger\ket{\tilde\Psi}=\ket\Psi$
> $\braket{x|\Psi}=\psi(x)$
> $\braket{x|\tilde\Psi}=\tilde\psi(x)$

For gauge invariance:
> $\partial_t\Lambda=0$
> $\tilde\Phi=\Phi$ (due to lambda time independence)
> $\tilde A(x)=\vec A(x)+\nabla\Lambda(x)$

Assuming the following is true for the non-tilde physics:
> $[\frac1{2m}(-i\hbar\nabla-q\vec A(x))^2+q\Phi(x)]\braket{x|\Psi}=E\braket{x|\Psi}=\braket{x|\hat H|\Psi}$
> $\hat H=\frac1{2m}(\vec p-q\vec A(x))^2+q\Phi(x)$ (x commutes and $-i\hbar\nabla\braket{x|\Psi}=\braket{x|\vec p|\Psi}$)

We'll start with an easy identity:
> $E=E\int dx|\braket{x|\Psi}|^2$
> $=\braket{\Psi|(\int dx|x}\braket{x|)E|\Psi}$
> $=\braket{\Psi|\hat H|\Psi}$
> $=\braket{\tilde\Psi|\hat U[\frac1{2m}(\vec p-q\vec A(x))^2+q\Phi(x)]\hat U^\dagger|\tilde\Psi}$
> $=\braket{\tilde\Psi|\hat U[\frac1{2m}(\vec p-q\vec A(x))^2\hat U^\dagger+\hat U^\dagger q\Phi(x)]|\tilde\Psi}$

For ease of access, let's compute how $\hat U^\dagger$ filters through the em-vee momentum:
> $(\hat p-q\hat A(x))\hat U^\dagger$
> $=(\hat p\hat U^\dagger-q\hat A(x)\hat U^\dagger)$
> $=(\hat p\hat U^\dagger-\hat U^\dagger q\hat A(x))$ (A and U are both functions of x)
> $=([\hat p,\hat U^\dagger]+\hat U^\dagger\vec p-\hat U^\dagger q\hat A(x))$
> $=([\hat p,\hat x]\nabla\hat U^\dagger+\hat U^\dagger\vec p-\hat U^\dagger q\hat A(x))$ (lemma derivative thingy)
> $=((-i\hbar)(-iq\nabla\Lambda(x)/\hbar)\hat U^\dagger+\hat U^\dagger\vec p-\hat U^\dagger q\hat A(x))$
> $=(-q\nabla\Lambda(x)\hat U^\dagger+\hat U^\dagger\vec p-\hat U^\dagger q\hat A(x))$
> $=(-\hat U^\dagger q\nabla\Lambda(x)+\hat U^\dagger\vec p-\hat U^\dagger q\hat A(x))$
> $=\hat U^\dagger(-q\nabla\Lambda(x)+\vec p-q\hat A(x))$
> $=\hat U^\dagger(\vec p-q\hat A(x)-q\nabla\Lambda(x))$
> $=\hat U^\dagger(\vec p-q\tilde A(x))$

And we can continue:
> $=\braket{\tilde\Psi|\hat U\hat U^\dagger[\frac1{2m}(\vec p-q\tilde A(x))^2+q\Phi(x)]|\tilde\Psi}$
> $=\braket{\tilde\Psi|[\frac1{2m}(\vec p-q\tilde A(x))^2+ q\Phi(x)]|\tilde\Psi}$
> $=\braket{\tilde\Psi|\tilde H|\tilde\Psi}$

> $\boxed{E\braket{x|\tilde \Psi}=\braket{x|\tilde H|\tilde \Psi}=[\frac1{2m}(-i\hbar\nabla-q\tilde A(x))^2+q\Phi(x)]\braket{x|\tilde\Psi}}$