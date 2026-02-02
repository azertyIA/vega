#PY511 
The first of five [[QM Axioms]].
## Rays
There's only one rule:
> $\ket{n}=\alpha\ket{n},\alpha\in\mathbb{C},\alpha\neq0$

Imagine a line, where particles in boxes contain their bounds in square brackets. The Riemann Integral has you partition out the dimension to different infinitesimal chunks. But most people need discontinuous "pulses." So, measure theory discretizes the range, and then solve the problem.

If you try to integrate a square and then shrink the square down, you get a delta distribution. In d dimensions you get a:
> $\bar L^2(\bar{\mathbb R}^d,\mathbb C)$

Consider a state localized at $x'\in\mathbb R$. There exists a Hermitian operator $\hat x$ such that:
> $\hat x\ket{x'}=x'\ket{x'}$

This means that $\ket{x'}$ is an eigenstate of $\hat x$ with eigenvalue $x$. The symbol inside the ket is just a label. Usually Sakurai uses that symbol as the eigenvalue as well. Meanwhile, the non-ket $x'$ is a real value. And $\hat x$ is an operator.

Let's define the wavefunction: 
> $\psi(x')=\braket{x'|\psi}$

You need complex numbers because it's the only way probability works. The only probability of a density gets 1. So now we have the following:
> ket $\ket\psi$, bra $\bra\psi$
> $\psi(x)=\braket{x|\psi}$
> $\hat x\ket{x'}=x'\ket{x'}$
> $\bra{x'}\hat x=\bra{x'}x'$
> $||\psi||^2=\int dx\psi^*(x)\psi(x)=1$

So let's talk about that last guy again, dx is a real number:
> $\int \braket{\psi|x}\braket{x|\psi}dx=1$
> $\bra{\psi}(\int \ket{x}\bra{x}dx)\ket{\psi}=1$, ($\braket{\psi|\psi}=1$)
> $\int dx\ket{x}\bra{x}=I$

What about the Momentum operator? There exists a Hermitian operator $\hat p$ such that:
> $[\hat x,\hat p]=i\hbar$
> $\Delta x\Delta p=\hbar/2$

Let's define another operator:
> $\hat T(a,\hat p)=\exp[\frac{-i}\hbar a\hat p]$
> $\hat T^\dagger(a,\hat p)=\exp[\frac{+i}\hbar a\hat p]$

So $\hat T$ is not Hermitian. But it can be rewritten as such:
> $\hat T^\dagger(a,\hat p)=\hat T(-a,\hat p)$
> $\hat T^\dagger(a,\hat p)\hat T(a,\hat p)=1$

So it's unitary. But what does it do? We only have one operator $\hat x$.
> $\hat T(a,\hat p)\ket{x'}=?$
> $\hat x\hat T(a,\hat p)\ket{x'}=([\hat x,\hat T(a,\hat p)]+\hat T(a,\hat p)\hat x)\ket{x'}$

So what is $[\hat x,\hat T(a,\hat p)]$? Using that one unused Lemma:
> $[\hat x,\hat T(a,\hat p)]=[\hat x,\hat p](\frac{-ia}\hbar)\hat T(a,\hat p)$
> $=a\hat T(a,\hat p)$

> $[\hat x,\hat T(a,\hat p)]\ket{x'}+\hat T(a,\hat p)\hat x\ket{x'}$
> $=a\hat T(a,\hat p)\ket{x'}+\hat T(a,\hat p)\hat x\ket{x'}$
> $=a\hat T(a,\hat p)\ket{x'}+\hat T(a,\hat p)x\ket{x'}$
> $=a\hat T(a,\hat p)\ket{x'}+x\hat T(a,\hat p)\ket{x'}$
> $=(a+x)\hat T(a,\hat p)\ket{x'}$
> $\hat T(a)\ket{x'}$ is a eigenstate of the position operator: $\ket{x'+a}$
### Translation
Now the T operator literally means that the position is translated. What else do we have? It's unitary:
> $\hat T^\dagger(a)=\hat T(-a)=\hat T^{-1}(a)$

$\hat T(a,\hat p)$ literally takes us from one localized state to another. Meanwhile (in case 1) the time can also be translated via the time evolutionary operator:
> $T(a,\hat p)=e^{-ia\hat p/\hbar}$
> $U(t,t_0=0)=e^{-i\hat Ht/\hbar}$

How does it apply to dual kets?
> $\bra{x'}\hat T(a)=?$
> $\hat T(b)\ket{x'}=\ket{x'+b}$
> $\bra{x'}\hat T(-b)=\bra{x'+b}$
> $\bra{x'}\hat T(a)=\bra{x'-a}$

In the adjoint space you just go the other way. But let's take some time to explore the momentum operator:
> $\hat p\ket{p'}=p'\ket{p'}$

This could in theory be represented in terms of a different basis like $\braket{x|\psi}$, as the position is a complete SOB.

> $\hat T(a)\ket{x'}=\ket{x'+a}$
> $\bra{x'}\hat T(a)^\dagger=\bra{x'+a}$
> $=\bra{x'}(1+ia\hat p/\hbar+\dots)$

Now consider a general waveket $\ket\Psi$, now we can use the translation operator:
> $\braket{x'+a|\Psi}=\braket{x'|\Psi}+ia\braket{x'|\hat p|\Psi}/\hbar+\dots$
> $=\braket{x'|\Psi}+ia\braket{x'|\hat p|\Psi}/\hbar+\dots$

Let's apply this expression to a specific eigenstate.
> $\ket\Psi=\ket{p'}$
> $\braket{x'+a|p'}$
> $=\braket{x'|p'}+ia\braket{x'|\hat p|p'}/\hbar+\dots$
> $=\braket{x'|p'}+ia\braket{x'|p'|p'}/\hbar+\dots$
> $=\braket{x'|p'}+iap'\braket{x'|p'}/\hbar+\dots$
> $=(1+iap'/\hbar+\dots)\braket{x'|p'}$

Let's try to shrink this $a$.
> $\lim_{a\to0}\frac{\braket{x'+a|p'}-\braket{x'|p'}}a=ip'/\hbar\braket{x'|p'}$
> $\partial_{x'}\braket{x'|p'}=ip'/\hbar\braket{x'|p'}$
> $\braket{x'|p'}=N\exp ip'x'/\hbar=\Phi_x(p')$

Let's find this normalization factor:
> $\int dp'|\Phi_x(p')|^2=1$
> $N=1/\sqrt{2\pi\hbar}$

So 
> $T(dx')=\exp[-i\hat pdx'/\hbar]=1-i\hat pdx'/\hbar$

### Fourier Transforms
> $g(k)=\int dxf(x)e^{-ikx}$
> $f(\omega)=\int dtf(t)e^{+i\omega x}$
> $\iint dxdt\Psi(x,t)e^{-i(kx-\omega t)}$
> $\iint d\vec rdt\Psi(\vec r,t)e^{-i(k\cdot x-\omega t)}$

This is important:
> $\delta(x)=\frac1{2\pi}\int dx 1e^{-ikx}$
### Harmonic Oscillators
> $\hat H=\frac{\hat p^2}{2m}+\frac12m\omega_0^2\hat x^2$
> $E_n=(n+\frac12)\hbar\omega_0$
> $\braket{x|n}=\psi(x)$

There are also creation and annihilation operators.
> $\hat H=\hbar\omega_0[\frac1{2m\hbar\omega_0}\hat p^2+\frac{m\omega_0}{2\hbar}\hat x^2]$
> $\hat x=\Delta_x(\hat a^\dagger+\hat a)$
> $\hat p=\Delta_p(\hat a^\dagger-\hat a)$
> $\Delta x\Delta p\geq\frac\hbar2=\Delta_x\Delta_p$
> $[\hat x,\hat p]=i\hbar$
> $[\hat a,\hat a^\dagger]=1$
> $\hat a^\dagger\hat a=\hat N$
> $\hat H=\hbar\omega_0(\hat N+\frac12)=\frac12\hbar\omega_0(\hat a\hat a^\dagger+\hat a^\dagger\hat a)$
