## 7.1. Exponentials

Given the following ground state wavefunction:
> $\braket{x|0}=(\frac{m\omega_0}{\pi\hbar})^{1/4}e^{-m\omega_0x^2/2\hbar}$
> $=(1/\pi x_0^2)^{1/4}\exp[-(x/x_0)^2/2]$ ($x_0^2=\hbar/m\omega_0$)

And the following formula:
> $f(\lambda)=\int dx\exp[\lambda x^2]$
> $f'(\lambda)=\int dxx^2\exp[\lambda x^2]$
> $=\partial_\lambda\int dx\exp[\lambda x^2]$
> $=\partial_\lambda\sqrt{\pi/\lambda}$
> $=-\sqrt\pi/2\sqrt\lambda^3$

Leading to the following value:
> $\braket{0|\hat x^2|0}=\int dx\braket{0|\hat x^2|x}\braket{x|0}$
> $=\int dx\braket{0|x^2|x}\braket{x|0}$
> $=\int dx\braket{0|x}\braket{x|0}x^2$
> $=(1/x_0\sqrt\pi)\int dxx^2\exp[-x^2/x_0^2]$
> $=(1/x_0)(x_0^3/2)$ ($\lambda=-1/x^2_0$)
> $=x_0^2/2$

Show that for the one-dimensional simple harmonic oscillator:
> $\braket{0|e^{ik\hat x}|0}=\int dx'\braket{0|e^{ik\hat x}\ket{x'}\bra{x'}0}$
> $=\int dx'\braket{0|e^{ik\hat x}\ket{x'}\bra{x'}0}$
> $=\int dx'\braket{0|e^{ikx'}\ket{x'}\bra{x'}0}$
> $=\int dx'\braket{0\ket{x'}\bra{x'}0}e^{ikx'}$
> $=\int dx'|\braket{0|x'}|^2e^{ikx'}$
> $=\int dx'(1/\pi x_0^2)^{1/2}\exp[-(x'/x_0)^2+ikx']$
> $=\int dx'\exp[-(x'/x_0)^2+ikx']/\sqrt\pi x_0$
> $=\int dx'\exp[-((x'/x_0)^2-ikx'-k^2x_0^2/4)-k^2x_0^2/4]/\sqrt\pi x_0$
> $=\int dx'\exp[-(x'/x_0-ikx_0/2)^2-k^2x_0^2/4]/\sqrt\pi x_0$
> $=(e^{-k^2x_0^2/4}/\sqrt\pi x_0)\int dx'\exp[-(x'/x_0)^2]$
> $=\exp[{-k^2x_0^2/4}]$
> $=\exp[{-k^2(x_0^2/2)/2}]$
> $=\exp[{-\frac{k^2}2\braket{0|\hat x^2|0}}]$

b. What about the wavenumber operator?
> $\braket{0|e^{ix\hat k}|0}=\int dx\braket{0|e^{ix\hat k}\ket{x}\bra{x}0}$

To preface:
> $\hat p\ket k=\hbar\hat k\ket k=\hbar k\ket k=p\ket k$
> $[\hat x,\hat p]=i\hbar$
> $\bra x[\hat x,\hat p]\ket {x'}=\bra x(\hat x\hat p-\hat p\hat x)\ket {x'}=i\hbar\braket{x|x'}$
> $=\bra x\hat x\hat p\ket {x'}-\bra x\hat p\hat x\ket {x'}$
> $=x\bra x\hat p\ket {x'}-x'\bra x\hat p\ket {x'}$
> $=(x-x')\bra x\hat p\ket {x'}=i\hbar\delta(x-x')$
> $=i\hbar\delta(x-x')\partial_x(x-x')$
> $=i\hbar(\partial_x(\delta(x-x')(x-x'))-\partial_x\delta(x-x')(x-x'))$
> $=i\hbar(-\partial_x\delta(x-x')(x-x'))$
> $(x-x')(-i\hbar\partial_x\delta(x-x'))=(x-x')\braket{x|\hat p|x'}$
> $\braket{x|\hat p|x'}=-i\hbar\partial_x\delta(x-x')$

We can apply this to a ket by the completeness identity:
> $\braket{x|\hat p(1)|\psi}=\int dx'\braket{x|\hat p|x'}\braket{x'|\psi}$
> $=-i\hbar\int dx'\partial_x\delta(x-x')\braket{x'|\psi}$
> $=-i\hbar\partial_x\int dx'\delta(x-x')\braket{x'|\psi}$ (most of it is a function of x')
> $=-i\hbar\partial_x\braket{x|\psi}$ (delta selection)
> $\braket{x|\hat k|\psi}=-i\partial_x\braket{x|\psi}$

But first, let's see what the expectation value is for the ground state:
> $\braket{0|\hat k^2|0}=\int dx\braket{0|x}\braket{x|\hat k^2|0}$
> $=-\int dx\braket{0|x}\partial_x^2\braket{x|0}$
> $=-\int dx\braket{0|x}\partial_x^2\exp[-x^2/2x_0^2]$
> $=-\int dx\braket{0|x}\partial_x(-x/x_0^2\cdot\exp[-x^2/2x_0^2])$
> $=\int dx\braket{0|x}(\partial_xx/x_0^2\cdot\exp[-x^2/2x_0^2]+x/x_0^2\cdot\partial_x\exp[-x^2/2x_0^2])$
> $=\int dx\braket{0|x}(1/x_0^2\cdot\exp[-x^2/2x_0^2]-(x/x_0^2)^2\cdot\exp[-x^2/2x_0^2])$
> $=\int dx\braket{0|x}(1/x_0^2-(x/x_0^2)^2)\exp[-x^2/2x_0^2]$
> $=\int dx\braket{0|x}(1/x_0^2-(x/x_0^2)^2)\braket{x|0}$
> $=\int dx\braket{0|x}\braket{x|0}(1/x_0^2-(x/x_0^2)^2)$
> $=(1/x_0^2)(1/\sqrt\pi x_0)\int dx\exp[-(x/x_0)^2](1-(x/x_0)^2)$
> $=(1/x_0^2)(1/\sqrt\pi x_0)(\int dx\exp[-(x/x_0)^2]-\int dx\exp[-(x/x_0)^2](x/x_0)^2)$
> $=(1/x_0^2)(1/\sqrt\pi x_0)(\sqrt\pi x_0-x_0\int duu^2\exp[-u^2])$
> $=(1/x_0^2)(1/\sqrt\pi x_0)(\sqrt\pi x_0-x_0\sqrt\pi/2)$
> $=(1/x_0^2)(1/\sqrt\pi x_0)(\sqrt\pi x_0/2)$
> $=1/2x_0^2$

Now we can apply it in from earlier:
> $\braket{0|e^{ix'\hat k}|0}=\int dx\braket{0|x}\braket{x|e^{ix'\hat k}|0}$
> $=\int dx\braket{0|x}\braket{x|(1+ix'\hat k-x'^2\hat k^2/2+\dots)|0}$
> $=\int dx\braket{0|x}(1+x'\partial_x+x'^2\partial_x^2/2+\dots)\braket{x|0}$
> $=\int dx\braket{0|x}\exp[x'\partial_x]\braket{x|0}$

What a weird operator thing I wonder what it does...
> $\exp[x'\partial_x]x^n=\Sigma\frac{x'^k}{k!}\partial_x^kx^n$
> $=\Sigma\frac{x'^k}{k!}\partial_x^kx^n$
> $=\Sigma x'^kx^{n-k}n!/k!(n-k)!$
> $=\Sigma\begin{pmatrix}n\\ k\end{pmatrix}x'^kx^{n-k}$
> $=(x+x')^n$

And looks like it just translates it some amount.
> $\int dx\braket{0|x}\exp[x'\partial_x]\braket{x|0}$
> $=\int dx\braket{0|x}\braket{x+x'|0}$
> $=(1/\sqrt\pi x_0)\int dx\exp[-x^2/2x_0^2]\exp[-(x+x')^2/2x_0^2]$
> $=(1/\sqrt\pi x_0)\int dx\exp[-(x^2+(x+x')^2)/2x_0^2]$
> $=(1/\sqrt\pi x_0)\int dx\exp[-(2x^2+2xx'+x'^2)/2x_0^2]$
> $=(1/\sqrt\pi x_0)\int dx\exp[-(2x^2+2xx'+x'^2/2+x'^2-x'^2/2)/2x_0^2]$
> $=(1/\sqrt\pi x_0)\int dx\exp[-2(x+x'/2)^2+x'^2/2)/2x_0^2]$
> $=(1/\sqrt\pi x_0)\exp[-x'^2/4x_0^2]\int dx\exp[-(x+x'/2)^2/x_0^2]$
> $=(1/\sqrt\pi x_0)\exp[-x'^2/4x_0^2]\int dx\exp[-x^2/x_0^2]$
> $=\exp[(-x'^2/2)(1/2x_0^2)]$
> $=\exp[\frac{-x^2}{2}\braket{0|\hat k^2|0}]$
## 7.2. Momentum Space

Given:
> $V(x)=-\lambda\delta(x)$, $\lambda>0$
> $\hat H=\hat p^2/2m-\lambda\delta(x)$
> $1=\int du\ket{u}\bra{u}$
> $u\delta(u)=0$
> $\braket{u|u'}=\delta(u-u')$

Let's start with this from last problem:
> $\braket{x|\hat p|\psi}=-i\hbar\partial_x\braket{x|\psi}$

So what if $\ket\psi$ was a momentum eigenstate $\ket k$?
> $\braket{x|\hat p|k}=\braket{x|\hbar k|k}=\hbar k\braket{x|k}=-i\hbar\partial_x\braket{x|k}$

Now we have a differential equation with an easy solution:
> $ik\braket{x|k}=\partial_x\braket{x|k}$
> $\braket{x|k}=Ae^{ikx}$

To find the normalization, just use the known relation:
> $\braket{k|k'}=\delta(k-k')$
> $=\int dx\braket{k|x}\braket{x|k'}$
> $=|A|^2\int dxe^{-ikx}e^{ik'x}$
> $=|A|^2\int dxe^{i(k'-k)x}$ (long integral)
> $=|A|^22\pi\delta(k-k')=\delta(k-k')$
> $|A|^2=1/2\pi$

Now let's actually begin the question.
> $E\braket{k|\psi}=\braket{k|E|\psi}=\braket{k|\hat H|\psi}$
> $=\braket{k| \hat p^2/2m-\lambda\delta(\hat x) |\psi}$
> $=\braket{k|\hat p^2/2m|\psi}-\braket{k|\lambda\delta(\hat x)|\psi}$
> $=\braket{k|\hbar^2k^2/2m|\psi}-\braket{k|\lambda\delta(\hat x)|\psi}$
> $=(\hbar^2k^2/2m)\braket{k|\psi}-\lambda\braket{k|\delta(\hat x)|\psi}$

> $\braket{k|\delta(\hat x)(1)|k'}=\int dx\braket{k|\delta(\hat x)|x}\braket{x|k'}$
> $=\int dx\braket{k|\delta(x)|x}\braket{x|k'}$
> $=\int dx\delta(x)\braket{k|x}\braket{x|k'}$
> $=|A|^2\int dx\delta(x)e^{-ikx}e^{ik'x}$
> $=|A|^2\int dx\delta(x)e^{i(k'-k)x}$
> $=|A|^2e^{i(k'-k)0}$
> $=1/2\pi$

> $\bra{k}\delta(\hat x)(1)\ket\psi=\bra k\delta(\hat x)\int dk'\ket{k'}\braket{k'|\psi}$
> $=\int dk'\bra k\delta(\hat x)\ket{k'}\braket{k'|\psi}$
> $=(1/2\pi)\int dk'\braket{k'|\psi}$

> $E\braket{k|\psi}=(\hbar^2k^2/2m)\braket{k|\psi}-(\lambda/2\pi)\int dk'\braket{k'|\psi}$
> $(\hbar^2k^2/2m-E)\braket{k|\psi}=(\lambda/2\pi)\int dk'\braket{k'|\psi}=C$

> $\braket{k|\psi}=C/(\hbar^2k^2/2m-E)$ (E < 0, for bound state)
> $=2mC/(\hbar^2(k^2+k_0^2))$

> $C=(\lambda/2\pi)\int dk\braket{k|\psi}$
> $=(\lambda mC/\pi\hbar^2)\int dk/(k^2+k_0^2)$
> $=(\lambda mC/\pi\hbar^2)\arctan(u)|_0^\infty$
> $=(\lambda mC/\hbar^2k_0)$
> $k_0=\lambda m/\hbar^2$ (momentum associated with bound state)
> $E=-\lambda^2m/2\hbar^2$

> $1=\int dk|\braket{k|\psi}|^2$
> $=\int dk|2mC/(\hbar^2(k^2+k_0^2))|^2$
> $=4m^2C^2/\hbar^4\int dk/(k^2+k_0^2)^2$
> $=4m^2C^2/\hbar^4k_0^3\int_{-\pi/2}^{\pi/2} du\sec^2(u)/(\tan^2(u)+1)^2$
> $=4m^2C^2/\hbar^4k_0^3\int du\sec^2(u)/\sec^4(u)$
> $=4m^2C^2/\hbar^4k_0^3\int du\cos^2(u)$
> $=2m^2C^2/\hbar^4k_0^3\int du(1+\cos2u)$
> $=2m^2C^2\pi/\hbar^4k_0^3$
> $=2m^2C^2\pi/\hbar^4k_0^3$
> $C=\hbar^2\sqrt{k_0^3/2\pi}/m$
> $\braket{k|\psi}=\sqrt{2k_0^3/\pi}/(k^2+k_0^2)$, $k_0=\lambda m/\hbar^2$

b. Consider the non-relativistic Particle-in-a-box problem:
> $\hat H=\hat p^2/2m+\hat V(x)$
> $\hat V(x)=\{0,\infty\}$

As tedious as this is, it feels like the only thing that makes sense to me nowadays:
> $(-\hbar^2\partial_x^2/2m)\braket{x|\Psi,t}=i\hbar\partial_t\braket{x|\Psi,t}$
> $(-\hbar^2\partial_x^2/2m)\psi(x)=E\psi(x)$
> $(E+\hbar^2\partial_x^2/2m)\psi(x)=0$
> $(E+\hbar^2\lambda^2/2m)=0$
> $\lambda_\pm=\pm\sqrt{-2mE/\hbar^2}$
> $\psi(x)=c_1e^{\lambda_+ x}+c_2e^{\lambda_-x}$
> $=B\cos(\lambda x)+A\sin(\lambda x)$
> $=A\sin(|\lambda|x)$ (doesn't exist at x=0)

Given $E_2=4\pi^2\hbar^2/2ma^2$:
> $\lambda=\sqrt{4\pi^2/a^2}$
> $\lambda=2\pi/a$
> $\psi(x)=A\sin(2\pi x/a)$
> $\int_0^adx|\psi(x)|^2=A^2\int_0^adx\sin^2(2\pi x/a)=1$
> $A^2=1/\int_0^adx\sin^2(2\pi x/a)=2/a$
> $\psi_2(x)=\braket{x|2}=\sqrt{2/a}\sin(2\pi x/a)$

Armed with this: $\braket{x|k}=\sqrt{1/2\pi}e^{ikx}\to\braket{x|p}=\sqrt{1/2\pi\hbar}e^{ipx/\hbar}$
> $\braket{p|(1)|2}=\int dx\braket{p|x}\braket{x|2}$
> $=\sqrt{1/a\pi\hbar}\int_0^a dxe^{-ipx/\hbar}\sin(2\pi x/a)$
> $=(\sqrt{1/a\pi\hbar})(1/2i)\int_0^a dx(e^{+i2\pi x/a}-e^{-i2\pi x/a})e^{-ipx/\hbar}$
> $=(\sqrt{1/a\pi\hbar})(1/2i)\int_0^a dx(\exp[{+i2\pi x/a-ipx/\hbar}]-\exp[{-i2\pi x/a-ipx/\hbar}])$
> $=(\sqrt{1/a\pi\hbar})(1/2i)\int_0^a dx(\exp[{-i(-2\pi /a+ip/\hbar})x]-\exp[-i(2\pi/a+ip/\hbar)x])$
> $=(\sqrt{1/a\pi\hbar})(1/2)((e^{-i(-2\pi /a+p/\hbar)a}-1)/(-2\pi /a+p/\hbar)-(e^{-i(2\pi/a+p/\hbar)a}-1)/(2\pi/a+p/\hbar))$
> $=(\sqrt{1/a\pi\hbar})(1/2)((e^{-i(-2\pi+pa/\hbar)}-1)/(-2\pi /a+p/\hbar)-(e^{-i(2\pi+pa/\hbar)}-1)/(2\pi/a+p/\hbar))$
> $=(\sqrt{1/a\pi\hbar})(1/2)((e^{-ipa/\hbar}-1)/(-2\pi /a+p/\hbar)-(e^{-ipa/\hbar}-1)/(2\pi/a+p/\hbar))$
> $=(\sqrt{1/a\pi\hbar})(1/2)(1-e^{-ipa/\hbar})(1/(2\pi/a+p/\hbar)+1/(2\pi /a-p/\hbar))$
> $=(\sqrt{1/a\pi\hbar})(1/2)(1-e^{-ipa/\hbar})(4\pi/a)/((2\pi/a)^2-(p/\hbar)^2)$
> $=(\sqrt{1/a\pi\hbar})(1-e^{-ipa/\hbar})(2\pi/a)/((2\pi/a)^2-(p/\hbar)^2)$

For the main calculation:
> $dW(p)=|\braket{p|2}|^2dp$
> $=(1/a\pi\hbar)(1-e^{-ipa/\hbar})(1-e^{+ipa/\hbar})(4\pi^2/a^2)/((2\pi/a)^2-(p/\hbar)^2)^2dp$
> $=(1/a\pi\hbar)(2-2\cos(pa/\hbar))(4\pi^2/a^2)/((2\pi/a)^2-(p/\hbar)^2)^2dp$
> $=(4\pi^2/a^3\pi\hbar)(2-2\cos(pa/\hbar))/((2\pi/a)^2-(p/\hbar)^2)^2dp$
> $=(16\pi^2/a^3\pi\hbar)(\sin^2(pa/2\hbar))/((2\pi/a)^2-(p/\hbar)^2)^2dp$
> $=(16\pi a/\hbar)(\sin^2(pa/2\hbar))/(4\pi^2-(pa/\hbar)^2)^2dp$

Or if $\hbar=1$:
> $dW(p)=(16\pi a)(\sin^2(pa/2))/(4\pi^2-(pa)^2)^2dp$
## 7.3. Bell's Inequality

Given that there are eight possible population (a, b, c each have two possibilities) of particle pairs one can reside in (do note that these represent the state of particle one, which is inverted to get the measurement of particle two to ensure 0 net angular momentum):
> $P(\hat a+;\hat b+)$ contains two populations ($a+,b-,c+$ and $a+,b-,c-$)
> $P(\hat a+;\hat c+)$ contains two populations ($a+,b+,c-$ and $a+,b-,c-$)
> $P(\hat b+;\hat c+)$ contains two populations ($a+,b+,c-$ and $a-,b+,c-$)

The probability of each case is equal to the size of the population divided by the size of the total, so the sizes of the contained populations can be compared to prove the inequality:
> $P(\hat a+;\hat b+)\leq P(\hat a+;\hat c+)+P(\hat c+;\hat b+)$ 
> $=N_{+-+}+N_{+--}\leq N_{++-}+N_{+--}+N_{+-+}+N_{--+}$ 
> ($N_{ijk}$ represent population with particle one state $ai,bj,ck$)
> $=N_{+-+}+N_{+--}\leq (N_{+--}+N_{+-+})+N_{++-}+N_{--+}$ 

Any $N$ is positive because it's just a population, and the right hand side is just the left hand side with extra positive numbers, so the relation must be true.

The significance of this inequality is that it offers a limit to classical mechanics which quantum mechanics experimentally violates. This allows for non-locality or "spooky action at a distance" in the real world.
## 7.4. Position Operators

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
> $=\Delta_x^2\frac12(2n+1)(e^{+i\omega t}+e^{-i\omega t})$
> $=\Delta_x^2(2n+1)(\cos\omega t)$

> $g_{x-}=\frac12(g_x(t,0)-g_x(0,t))$
> $=\Delta_x^2\frac12(-1)(e^{+i\omega t}-e^{-i\omega t})$
> $=-\Delta_x^2(\sin\omega t)$ (maybe)
## 7.5. Displacement

Consider the Displacement Operator:
> $\hat D(\alpha)=e^{\alpha\hat\alpha^\dagger-\alpha^*\hat\alpha}$

> $\hat D^\dagger(\alpha)\hat a\hat D(\alpha)$
> $=e^{\alpha^*\hat\alpha-\alpha\hat\alpha^\dagger}\hat a e^{\alpha\hat\alpha^\dagger-\alpha^*\hat\alpha}$
> $=\hat a+[\alpha a^*\hat a-\alpha\hat a^\dagger,\hat a]+\frac12\dots$
> $=\hat a+(\alpha^*\hat a-\alpha\hat a^\dagger)\hat a-\hat a(\alpha^*\hat a-\alpha\hat a^\dagger)+\frac12\dots$
> $=\hat a+\alpha^*\hat a\hat a-\alpha\hat a^\dagger\hat a-(\alpha^*\hat a\hat a-\alpha\hat a\hat a^\dagger)+\frac12\dots$
> $=\hat a-\alpha\hat a^\dagger\hat a+\alpha\hat a\hat a^\dagger+\frac12\dots$
> $=\hat a+\alpha[\hat a,\hat a^\dagger]+\frac12\dots$
> $=\hat a+\alpha+0+\dots$ (the commutator of a number is zero)

> $\hat D^\dagger(\alpha)\hat a^\dagger\hat D(\alpha)$
> $=\hat a^\dagger+[\alpha a^*\hat a-\alpha\hat a^\dagger,\hat a^\dagger]+\frac12\dots$
> $=\hat a+(\alpha^*\hat a-\alpha\hat a^\dagger)\hat a^\dagger-\hat a^\dagger(\alpha^*\hat a-\alpha\hat a^\dagger)+\frac12\dots$
> $=\hat a+\alpha^*\hat a\hat a^\dagger-\alpha\hat a^\dagger\hat a^\dagger-(\alpha^*\hat a^\dagger\hat a-\alpha\hat a^\dagger\hat a^\dagger)+\frac12\dots$
> $=\hat a+\alpha\hat a^\dagger\hat a-\alpha\hat a\hat a^\dagger+\frac12\dots$
> $=\hat a-\alpha[\hat a,\hat a^\dagger]+\frac12\dots$
> $=\hat a-\alpha+0+\dots$ (the commutator of a number is zero)

> $\hat D^\dagger(\alpha)\hat a\hat D(\alpha)$
> $=(\hat D(\alpha)\hat a^\dagger\hat D(\alpha)^\dagger)^\dagger$
> $=(\hat a-\alpha)^\dagger$
> $=\hat a^\dagger-\alpha^*$

> $\hat D^\dagger(\alpha)\hat a^\dagger\hat D(\alpha)$
> $=(\hat D(\alpha)\hat a^\dagger\hat D(\alpha)^\dagger)^\dagger$
> $=(\hat a-\alpha)^\dagger$
> $=\hat a^\dagger-\alpha^*$
