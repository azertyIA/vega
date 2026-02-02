## 7.1. Exponentials

Show that for the one-dimensional simple harmonic oscillator:
> $\braket{0|e^{ik\hat x}|0}=\exp(-\frac12k^2\braket{0|\hat x^2|0})$
> $=\braket{0|1+ik\hat x-\frac12k^2\hat x^2+\dots|0}$
> $=1+\braket{0|ik\hat x-\frac12k^2\hat x^2+\dots|0}$ (odd functions will expect to be zero)
> $=1+\braket{0|ik\hat x-\frac12k^2\hat x^2+\dots|0}$
> $=1-\braket{0|\frac12k^2\hat x^2|0}+\dots$
> $=\braket{0|0}-\braket{0|\frac12k^2\hat x^2|0}+\dots$
> $=\braket{0|0}-\frac12k^2\braket{0|\hat x^2|0}+\dots$

## 7.2. Momentum Space

Given:
> $V(x)=-\lambda\delta(x)$, $\lambda>0$
> $\hat H=\hat p^2/2m-\lambda\delta(x)$
> $\hat p\ket k=\hbar\hat k\ket k=\hbar k\ket k=p\ket k$

Assume that the $\ket k$ eigenstates form a complete SOB.
> $\ket\Psi=\Sigma c_n\ket {k_n}$

And assume 
## 7.3. Bell's Inequality

## 7.4. Position Operator

Consider the Heisenberg position operator:
> $\hat x=\Delta_x(\hat a+\hat a^\dagger)$
> $\hat H=\hbar\omega(\hat a^\dagger\hat a+\frac12)$

> $\hat x(t)_H=e^{i\hat Ht/\hbar}\hat xe^{-i\hat Ht/\hbar}$
> $=\Delta_xe^{i\hat Ht/\hbar}(\hat a+\hat a^\dagger)e^{-i\hat Ht/\hbar}$
> $=\Delta_x(e^{i\hat Ht/\hbar}\hat ae^{-i\hat Ht/\hbar}+e^{i\hat Ht/\hbar}\hat a^\dagger e^{-i\hat Ht/\hbar})$
> $=\Delta_x(\hat a_H+\hat a^\dagger_H)$

> $\partial_t\hat a_H=\frac i\hbar[\hat H,\hat a_H]$ (ladder properties still work because the time term cancels and surrounds)
> $=i\omega[\hat a_H^\dagger\hat a_H,\hat a_H]$
> $=i\omega(\hat a_H^\dagger[\hat a_H,\hat a_H]+[\hat a_H^\dagger,\hat a_H]\hat a_H)$
> $=i\omega(0-\hat a_H)$
> $=-i\omega\hat a_H$
> $\partial_t\hat a_H=-i\omega\hat a_H$ (solve this ODE)
> $\hat a_H(t)=e^{-i\omega t}\hat a_H(0)=e^{-i\omega t}\hat a$
> $\hat a^\dagger_H(t)=e^{i\omega t}\hat a_H^\dagger(0)=e^{i\omega t}\hat a^\dagger$

> $\hat x(t)_H=\Delta_x(\hat a_H+\hat a^\dagger_H)$
> $=\Delta_x(e^{-i\omega t}\hat a+e^{+i\omega t}\hat a^\dagger)$

> $\braket{n|\hat x_H(t)\hat x_H(0)|n}$
> $=\Delta_x^2\braket{n|e^{-i\omega t}\hat a\hat a+e^{+i\omega t}\hat a^\dagger\hat a+e^{-i\omega t}\hat a\hat a^\dagger+e^{+i\omega t}\hat a^\dagger\hat a^\dagger|n}$
> $=\Delta_x^2\braket{n|e^{+i\omega t}\hat a^\dagger\hat a+e^{-i\omega t}\hat a\hat a^\dagger|n}$ (double annihilation/creation changes ket, so that's 0)
> $=\Delta_x^2\braket{n|e^{+i\omega t}\hat N+e^{-i\omega t}([\hat a,\hat a^\dagger]+\hat N)|n}$
> $=\Delta_x^2\braket{n|e^{+i\omega t}\hat N+e^{-i\omega t}(1+\hat N)|n}$
> $=\Delta_x^2\braket{n|ne^{+i\omega t}+(n+1)e^{-i\omega t}|n}$
> $=\Delta_x^2(ne^{+i\omega t}+(n+1)e^{-i\omega t})$

> $\braket{n|\hat x_H(0)\hat x_H(t)|n}$
> $=\Delta_x^2\braket{n|e^{-i\omega t}\hat a\hat a+e^{+i\omega t}\hat a\hat a^\dagger+e^{-i\omega t}\hat a^\dagger\hat a+e^{+i\omega t}\hat a^\dagger\hat a^\dagger|n}$
> $=\Delta_x^2\braket{n|e^{+i\omega t}\hat a\hat a^\dagger+e^{-i\omega t}\hat a^\dagger\hat a|n}$
> $=\Delta_x^2\braket{n|(n+1)e^{+i\omega t}+ne^{-i\omega t}|n}$
> $=\Delta_x^2((n+1)e^{+i\omega t}+ne^{-i\omega t})$

> $g_{x+}=\frac12(g_x(t,0)+g_x(0,t))$
> $=\frac12(2n+1)\braket{n|e^{+i\omega t}+e^{-i\omega t}|n}$
> $=(2n+1)(\cos\omega t)$

> $g_{x-}=\frac12(g_x(t,0)-g_x(0,t))$
> $=\frac12\braket{n|-e^{+i\omega t}+e^{-i\omega t}|n}$
> $=(-\sin\omega t)$

Consider the Displacement Operator:
> $\hat D(\alpha)=e^{\alpha\hat\alpha^\dagger-\alpha^*\hat\alpha}$

> $\hat D^\dagger(\alpha)\hat\alpha\hat D(\alpha)$
> $=e^{\alpha^*\hat\alpha-\alpha\hat\alpha^\dagger}\hat\alpha e^{\alpha\hat\alpha^\dagger-\alpha^*\hat\alpha}$
> $=(1+\alpha^*\hat a-\alpha\hat a^\dagger+\dots)\hat a(1+\alpha\hat a^\dagger-\alpha^*\hat a+\dots)$
	
