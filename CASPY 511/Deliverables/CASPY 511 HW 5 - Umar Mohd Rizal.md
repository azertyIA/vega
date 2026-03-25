## 5.1. Instantaneous vs Adiabatic
Given:
> $V(x)=\frac12m\omega^2x^2-q\epsilon x$
> $\hat H=\frac{\hat p^2}{2m}+\hat V(x)=\frac{\hat p^2}{2m}\nabla^2+m\omega^2x^2-q\epsilon x$

a. Find the probability that the particle will remain in the ground state for time t > 0.
> $\hat H_{t<0}=\frac{\hat p^2}{2m}\nabla^2+\frac12m\omega^2x^2$

I did the solution for this in homework 3 using ladder operators.
> $\phi_{0,t<0}(x)=({m\omega_0}/{\pi\hbar})^{1/4}\exp({-m\omega_0x^2/2\hbar})$

For the new Hamiltonian:
> $\hat H=\frac{\hat p^2}{2m}\nabla^2+\frac12m\omega^2x^2-q\epsilon x$
> $=\frac{\hat p^2}{2m}\nabla^2+\frac12m\omega^2(x^2-2q\epsilon x/m\omega^2)$
> $=\frac{\hat p^2}{2m}\nabla^2+m\omega^2(x^2-2q\epsilon x/m\omega^2+q^2\epsilon^2/m^2\omega^4-q^2\epsilon^2/m^2\omega^4)$
> $=\frac{\hat p^2}{2m}\nabla^2+m\omega^2((x-q\epsilon/m\omega^2)^2-q^2\epsilon^2/m^2\omega^4)$
> $=\frac{\hat p^2}{2m}\nabla^2+m\omega^2(x-q\epsilon/m\omega^2)^2-q^2\epsilon^2/2m\omega^2$

The last term is just a constant which doesn't change the eigenvectors (it's fairly linear). The first term is just a part of the original Hamiltonian which is known not to change the eigenvectors. The middle term on the other hand represents a position translation as there is something put with the position operator when compared to the original Hamiltonian:
> $\hat H\ket x\approx\hat H_{t<0}\ket{x-q\epsilon/m\omega^2}$
> $\phi_0(x)=({m\omega_0}/{\pi\hbar})^{1/4}\exp({-m\omega_0(x-\alpha)^2/2\hbar})$

So to find the probability that the particle remains in the ground state, find the inner product of the two states:
> $\braket{\phi_{0}|\phi_{0,t<0}}$
> $=(m\omega/\pi\hbar)^{1/2}\int dx\exp[-\frac{m\omega}{2\hbar}((x-a)^2+x^2)]$
> $=(m\omega/\pi\hbar)^{1/2}\int dx\exp[-\frac{m\omega}{2\hbar}((x-a)^2+x^2)]$
> $=(m\omega/\pi\hbar)^{1/2}\int dx\exp[-\frac{m\omega}{2\hbar}(2x^2-2ax-a^2)]$
> $=(m\omega/\pi\hbar)^{1/2}\int dx\exp[-\frac{m\omega}{2\hbar}(2(x-a/2)^2-a^2/4)]$
> $=(\exp[-m\omega a^2/4\hbar])\int dx(m\omega/\pi\hbar)^{1/2}\exp[-\frac{m\omega}{\hbar}x^2]$ (x-a/2 can be translated to x on infinity)
> $=(\exp[-m\omega a^2/4\hbar])\int dx\phi_0(x)$
> $=\exp[-m\omega a^2/4\hbar]$ (definition of probability distribution)

So just square this to get the probability:
> $P=\exp[-m\omega a^2/2\hbar]=\exp[-q^2\epsilon^2/2m\hbar\omega^3]$

b. To see how a gradual change would impact the oscillator, just set the electric field to almost zero:
> $P=\exp[0]=1$
## 5.2. Rabi Probem
> $\hat H=\hat H_0+V$
> $\hat H_0=\epsilon_0\ket0\bra0+\epsilon_1\ket1\bra1$
> $\hat V=\gamma\exp(-i\omega t)\ket1\bra0+\gamma\exp(+i\omega t)\ket0\bra1$
> $\ket{\psi,t=0}=\ket0$
> $\ket{\psi,t}_I=\exp(iH_0t/\hbar)\ket{\psi,t}_S=c_0(t)\ket0+c_1(t)\ket1$

a. Find Eq 5.189.
> $i\hbar\partial_t\ket{\psi,t}_I=i\hbar\partial_t(\exp(iH_0t/\hbar)\ket{\psi,t}_S)$
> $=i\hbar\partial_t(\exp(iH_0t/\hbar))\ket{\psi,t}_S$
> $+\exp(iH_0t/\hbar)i\hbar\partial_t\ket{\psi,t}_S$
> $=-H_0\exp(iH_0t/\hbar)\ket{\psi,t}_S$
> $+\exp(iH_0t/\hbar)(H_0+V)\ket{\psi,t}_S$ (Hamiltonian)
> $=\exp(iH_0t/\hbar)(-H_0+H_0+V)\ket{\psi,t}_S$
> $=\exp(iH_0t/\hbar)(V)\ket{\psi,t}_S$
> $=\exp(+iH_0t/\hbar)(V)\exp(-iH_0t/\hbar)\ket{\psi,t}_I$ (reverse of interaction pic)

Taking the exponential terms:
> $\exp(+iH_0t/\hbar)$
> $=(\exp(+i\epsilon_0t/\hbar)\ket0\bra0+\exp(+i\epsilon_1t/\hbar)\ket1\bra1$

Now we just match up the terms (there's two):
> $\gamma(\exp(+i\epsilon_0t/\hbar)\ket0\bra0)(\exp(+i\omega t)\ket0\bra1)(\exp(-i\epsilon_1t/\hbar)\ket1\bra1)$
> $=\gamma\exp(+i\epsilon_0t/\hbar)\exp(+i\omega t)\exp(-i\epsilon_1t/\hbar)\ket0\bra1$
> $=\gamma\exp(+i((\epsilon_0-\epsilon_1)/\hbar+\omega)t)\ket0\bra1$
> $=\gamma\exp(-i(\omega_{10}-\omega)t)\ket0\bra1$, $\omega_{10}=(\epsilon_1-\epsilon_0)/\hbar$
> $\gamma(\exp(+i\epsilon_1t/\hbar)\ket1\bra1)(\exp(-i\omega t)\ket1\bra0)(\exp(-i\epsilon_0t/\hbar)\ket0\bra0)$
> $=\gamma\exp(+i\epsilon_1t/\hbar)\exp(-i\omega t)(\exp(-i\epsilon_0t/\hbar)\ket1\bra0$
> $=\gamma\exp(+i((\epsilon_1-\epsilon_0)/\hbar-\omega)t)\ket1\bra0$
> $=\gamma\exp(+i(\omega_{10}-\omega)t)\ket1\bra0$, $\omega_{10}=(\epsilon_1-\epsilon_0)/\hbar$

And the result:
> $\hat V_I(t)=\begin{pmatrix}0&\gamma\exp(+i(\omega-\omega_{10})t)\\\gamma\exp(-i(\omega-\omega_{10})t)&0\end{pmatrix}$
> $i\hbar\partial_t\ket{\psi,t}_I=\begin{pmatrix}0&\gamma\exp(+i(\omega-\omega_{10})t)\\\gamma\exp(-i(\omega-\omega_{10})t)&0\end{pmatrix}\ket{\psi,t}_I$

b. Derive the Rabi formula for the time dependent probability from $\ket0\to\ket1$
> $i\hbar\partial_tc_0(t)=\gamma\exp(+i\mu t)c_1(t)$, $\mu=\omega-\omega_{10}$
> $i\hbar\partial_tc_1(t)=\gamma\exp(-i\mu t)c_0(t)$
> $(i\hbar\partial_t)^2c_1(t)=i\hbar\partial_t\gamma\exp(-i\mu t)c_0(t)$
> $=\gamma i\hbar\partial_t\exp(-i\mu t)c_0(t)+\gamma\exp(-i\mu t)(i\hbar\partial_tc_0(t))$
> $=\mu\hbar(\gamma\exp(-i\mu t)c_0(t))+\gamma\exp(-i\mu t)(\gamma\exp(+i\mu t)c_1(t))$
> $=i\mu\hbar^2\partial_tc_1(t)+\gamma^2c_1(t)$

Solving the differential equation:
> $(i\hbar\partial)^2c_1(t)-i\mu\hbar^2\partial_tc_1(t)-\gamma^2c_1(t)=0$
> $\partial^2c_1(t)+i\mu\partial_tc_1(t)+(\gamma/\hbar)^2c_1(t)=0$
> $\lambda^2+i\mu\lambda+(\gamma/\hbar)^2=0$
> $\lambda=(-i\mu\pm\sqrt{-\mu^2-4\gamma^2/\hbar^2})/2$

Given that $\Omega:=\sqrt{4\gamma^2/\hbar^2+\mu^2}$
> $\lambda=-i(\mu\pm\Omega)/2$
> $c_1(t)=A\exp[-i(\mu-\Omega)t/2]+B\exp[-i(\mu+\Omega)t/2]$
> $=A\exp[-i(\mu-\Omega)t/2]+B\exp[-i(\mu+\Omega)t/2]$

> $c_1(0)=0=A+B$, $A=-B$
> $\partial_tc_1(0)=\gamma/i\hbar=\lambda_+A-\lambda_-A$
> $\gamma/i\hbar=(-i(\mu-\Omega)/2--i(\mu+\Omega)/2)A$
> $\gamma/i\hbar=i\Omega A$
> $-\gamma/\hbar\Omega=A$

> $=(-\gamma/\hbar\Omega)(\exp[-i(\mu-\Omega)t/2]-\exp[-i(\mu+\Omega)t/2])$
> $=(-\gamma/\hbar\Omega)\exp[-i\mu t/2](\exp[i\Omega t/2]-\exp[-i\Omega t/2])$
> $=(-2\gamma/\hbar\Omega)\exp[-i\mu t/2](\sin\Omega t/2)$
> $=(-2\gamma/\hbar\Omega)\exp[-i\mu t/2](\sin\Omega t/2)$

> $|c_1(t)^2|=(4\gamma^2/\hbar^2\Omega^2)sin^2\Omega t/2$
> $=\frac{4\gamma^2/\hbar^2}{4\gamma^2/\hbar^2+(\omega-\omega_{10})^2}\sin^2(\sqrt{\frac{\gamma^2}{\hbar^2}+\frac14(\omega-\omega_{10})^2}t)$
## 5.3. Electron Paramagnetic Resonance
> $\vec B=B_0\hat z+B_1(\hat x\cos\omega t+\hat y\sin\omega t)$
> $\hat H=\hat H_0+V$
> $\hat H_0=\epsilon_0\ket0\bra0+\epsilon_1\ket1\bra1=-(e\hbar B_0/2mc)(\ket0\bra0-\ket1\bra1)$
> $\hat V=\gamma\exp(-i\omega t)\ket1\bra0+\gamma\exp(+i\omega t)\ket0\bra1$
> $=-(e\hbar B_1/2mc)[\cos\omega t(\ket1\bra0+\ket0\bra1)+i\sin\omega t(\ket0\bra1-\ket1\bra0)]$

a. For housekeeping:
> $\epsilon_0=-e\hbar B_0/2mc$
> $\epsilon_1=e\hbar B_0/2mc$
> $\gamma=-e\hbar B_1/2mc$

Plugging in values...
> $\omega_{10}=g_e\mu_eB_0/\hbar$
> $=(2)(9.274*10^{-24} J/T)(0.35 T)/(1.05*10^{-34} Js)$
> $=6.18*10^{10}$ rad/s
> $=9.8$ GHz 

b. I'm afraid I ran out of time to plot something
> $I=B^2/2\mu c$
> $B=86.8$ T
> $\gamma=2.68*10^{-30}$

c. If the RF frequency is off by that much then:
> Compare $\frac{4\gamma^2/\hbar^2}{4\gamma^2/\hbar^2+(\omega-\omega_{10})^2}$, and you end up getting that it's off by about 6-7 orders of magnitude lower.
## 5.4. Spin Me Right Round
Consider a general spin ket below along with its Bloch sphere representation.
> $\ket\Psi=\cos\frac\theta2\ket0+e^{i\phi}\sin\frac\theta2\ket1$

a.i. $\eta$ is a small angle. What does $\exp\frac{+i\eta}2\sigma_z$ do?
> $e^{\frac{+i\eta}2\sigma_z}$
> $=(I+\frac{+i\eta}{2}\sigma_z+\frac{-\eta^2}{4\cdot2!}I+\frac{-i\eta^3}{8\cdot3!}\sigma_z+\frac{\eta^4}{16\cdot4!}I+\dots)$
> $=(I+\frac{-\eta^2}{4\cdot2!}I+\frac{\eta^4}{16\cdot4!}I+\dots)+(\frac{+i\eta}{2}\sigma_z+\frac{-i\eta^3}{8\cdot3!}\sigma_z+\dots)$
> $=(1+\frac{-\eta^2}{4\cdot2!}+\frac{\eta^4}{16\cdot4!}+\dots)I+(\frac{+i\eta}{2}+\frac{-i\eta^3}{8\cdot3!}+\dots)\sigma_z$
> $=I\cos(\frac\eta2)+i\sigma_z\sin(\frac\eta2)$
> $=\begin{pmatrix}e^{+\eta/2}&0\\0&e^{-\eta/2}\end{pmatrix}$

That makes enough sense.
> $e^{\frac{+i\eta}2\sigma_z}\ket\Psi$
> $=e^{\frac{+i\eta}2}\cos\frac\theta2\ket0$
> $+e^{\frac{-i\eta}2}e^{i\phi}\sin\frac\theta2\ket1$

Only the phase is impacted as the resulting ket con be multiplied by a phase. 
> $e^{\frac{+i\eta}2\sigma_z}\ket\Psi=\cos\frac\theta2\ket0+e^{i(\phi-\eta)}\sin\frac\theta2\ket1$

This rotation only rotates it in phase or around the z axis by some angle $\eta$. To find which way it rotates, you can use the fact that it rotates the $\ket+$ ($\phi-\eta=0$) to the $\ket{-i}$ ($\phi-\eta=-\pi/2$), so from the top, the Block sphere rotates clockwise.

a.ii. Show that $\exp[-i\eta(\vec\sigma\cdot\vec n)/2]$ rotates it about the $\hat n$ axis by an angle.

I could run through other examples but I kind of ran out of time, so the fact that setting $\hat n=\hat z$ creates the opposite of the previous problem is indicative that this operation rotates the ket about the axis $\hat n$ but counter-clockwise according to the sign.

b. Prove that $\hat U(\eta)=\cos(\eta/2)I-i\sin(\eta/2)(\vec\sigma\cdot\hat n)$
> $\exp[-i\eta(\vec\sigma\cdot\vec n)/2]$, ($(\sigma\cdot n)^2=I$)
> $=(I-i\eta(\vec\sigma\cdot\vec n)/2+\dots)$
> $=(I-\eta^2/8+\dots)+i(-\eta/2+\dots)(\vec\sigma\cdot\vec n)$
> $=\cos(\eta/2)I-i\sin(\eta/2)(\vec \sigma\cdot \hat n)$
## 5.5. Perturbation
Given:
> $\hat H=\hat H_0+V$
> $\hat H_0=\epsilon_0\ket0\bra0+\epsilon_1\ket1\bra1$
> $\hat V_S=2V_0\cos\omega t\ket1\bra0+2V_0\cos\omega t\ket0\bra1$

a. Given
> $\ket{\Psi,t}_I=\exp(+iH_0t/\hbar)\ket{\Psi,t}_S$
> $=\exp(+iH_0t/\hbar)(c_0(t)\ket0+c_1(t)\ket1)$
> $=c_0(t)\exp(+iH_0t/\hbar)\ket0+c_1(t)\exp(+iH_0t/\hbar)\ket1$

One of these terms looks like:
> $c_0(t)\exp(+iH_0t/\hbar)\ket0$
> $=c_0(t)(1+iH_0t/\hbar+\dots)\ket0$
> $=c_0(t)(1+i(\epsilon_0\ket0\bra0+\epsilon_1\ket1\bra1)t/\hbar+\dots)\ket0$
> $=c_0(t)(1+i(\epsilon_0\ket0\braket{0|0}+\epsilon_1\ket1\braket{1|0})t/\hbar+\dots)$
> $=c_0(t)(1+i(\epsilon_0\ket0)t/\hbar+\dots)$
> $=c_0(t)(1+i\epsilon_0t/\hbar+\dots)\ket0$
> $=c_0(t)\exp(+i\epsilon_0t/\hbar)\ket0$

So two of these terms should be and after a phase shift:
> $=c_0(t)\exp(+i\epsilon_0t/\hbar)\ket0+c_1(t)\exp(+i\epsilon_1t/\hbar)\ket1$
> $=c_0(t)\ket0+c_1(t)\exp(+i(\epsilon_1-\epsilon_0)t/\hbar)\ket1$
> $=c_0(t)\ket0+c_1(t)\exp(+i\omega_{10}t)\ket1$, $\omega_{10}=(\epsilon_1-\epsilon_0)/\hbar$

a.ii. 
> $\hat V_I(t)=\exp(+iH_0t/\hbar)\hat V_S(t)\exp(-iH_0t/\hbar)$
> $=\exp(+iH_0t/\hbar)(2V_0\cos\omega t\ket1\bra0+2V_0\cos\omega t\ket0\bra1)\exp(-iH_0t/\hbar)$
> $=2V_0\exp(+iH_0t/\hbar)(\cos\omega t\ket1\bra0+\cos\omega t\ket0\bra1)\exp(-iH_0t/\hbar)$

Taking the exponential terms:
> $\exp(+iH_0t/\hbar)$
> $=(\exp(+i\epsilon_0t/\hbar)\ket0\bra0+\exp(+i\epsilon_1t/\hbar)\ket1\bra1$

Now we just match up the terms (there's two):
> $2V_0(\exp(+i\epsilon_0t/\hbar)\ket0\bra0)(\cos\omega t\ket0\bra1)(\exp(-i\epsilon_1t/\hbar)\ket1\bra1)$
> $=2V_0(\exp(+i\epsilon_0t/\hbar)(\cos\omega t)(\exp(-i\epsilon_1t/\hbar))\ket0\bra1$
> $=2V_0(\cos\omega t)\exp(-i\omega_{10}t)\ket0\bra1$
> $2V_0(\exp(+i\epsilon_1t/\hbar)\ket1\bra1)(\cos\omega t\ket1\bra0)(\exp(-i\epsilon_0t/\hbar)\ket0\bra0)$
> $=2V_0(\exp(+i\epsilon_1t/\hbar)(\cos\omega t)(\exp(-i\epsilon_0t/\hbar))\ket1\bra0$
> $=2V_0(\cos\omega t)\exp(+i\omega_{10}t)\ket1\bra0$

Putting the two together:
> $\hat V_I(t)=2V_0\cos\omega t\begin{pmatrix}0&\exp(-i\omega_{10}t)\\\exp(+i\omega_{10}t)&0\end{pmatrix}$
> $\hat V_I(t)=V_0(\exp(+i\omega t)+\exp(-i\omega t))\begin{pmatrix}0&\exp(-i\omega_{10}t)\\\exp(+i\omega_{10}t)&0\end{pmatrix}$
> $\hat V_I(t)=V_0\begin{pmatrix}0&(\exp(+i\omega t)+\exp(-i\omega t))\exp(-i\omega_{10}t)\\(\exp(+i\omega t)+\exp(-i\omega t))\exp(+i\omega_{10}t)&0\end{pmatrix}$
> $\hat V_I(t)=V_0\begin{pmatrix}0&\exp(+i(\omega-\omega_{10})t)+\exp(-i(\omega+\omega_{10}) t)\\\exp(+i(\omega+\omega_{10})t)+\exp(-i(\omega-\omega_{10}) t)&0\end{pmatrix}$
> $\hat V_I(t)=V_0(\exp(+i(\omega-\omega_{10})t)+\exp(-i(\omega+\omega_{10}) t))\ket0\bra1$
> $+V_0(\exp(+i(\omega+\omega_{10})t)+\exp(-i(\omega-\omega_{10}) t))\ket1\bra0$

b. Use the Dyson Series to calculate the Time Evolution Operator to the first order.
> $U_I(t)=I-\frac i\hbar\int^t_0dt'\hat V_I(t')$
> $=I-\frac {V_0i}\hbar\int^t_0dt'\hat V_I(t')$
> $=I-\frac {V_0i}\hbar\int^t_0dt'\hat V_I(t')$
> $=I$
> $-V_0i/\hbar\int dt'(\exp(+i(\omega-\omega_{10})t)+\exp(-i(\omega+\omega_{10}) t))\ket0\bra1$
> $-V_0i/\hbar\int dt'(\exp(+i(\omega+\omega_{10})t)+\exp(-i(\omega-\omega_{10}) t))\ket1\bra0$
> $=I$
> $-V_0i/\hbar\int dt'\exp(+i(\omega-\omega_{10})t)\ket0\bra1$
> $-V_0i/\hbar\int dt'\exp(-i(\omega+\omega_{10}) t)\ket0\bra1$
> $-V_0i/\hbar\int dt'\exp(+i(\omega+\omega_{10})t)\ket1\bra0$
> $-V_0i/\hbar\int dt'\exp(-i(\omega-\omega_{10}) t)\ket1\bra0$
> $=I+V_0/\hbar($
> $+(1-\exp(+i(\omega-\omega_{10})t))\ket0\bra1/(\omega-\omega_{10})$
> $-(1-\exp(-i(\omega+\omega_{10}) t))\ket0\bra1/(\omega+\omega_{10})$
> $+(1-\exp(+i(\omega+\omega_{10})t))\ket1\bra0/(\omega+\omega_{10})$
> $-(1-\exp(-i(\omega-\omega_{10}) t))\ket1\bra0/(\omega-\omega_{10}))$

c. Find $c_1^1(t):=\bra1U_I(t)\ket0$
> $=\bra1V_0/\hbar($
> $+(1-\exp(+i(\omega+\omega_{10})t))\ket1\bra0/(\omega+\omega_{10})$
> $-(1-\exp(-i(\omega-\omega_{10}) t))\ket1\bra0/(\omega-\omega_{10}))\ket0$
> $=V_0/\hbar($
> $+(1-\exp(+i(\omega+\omega_{10})t))/(\omega+\omega_{10})$
> $-(1-\exp(-i(\omega-\omega_{10}) t))/(\omega-\omega_{10}))$
> $=V_0/\hbar((1-\exp(+i(\omega+\omega_{10})t))/(\omega+\omega_{10})-(1-\exp(-i(\omega-\omega_{10}) t))/(\omega-\omega_{10}))$
> $=V_0/\hbar((1-\exp(+i(\omega_{10}+\omega)t))/(\omega+\omega_{10})+(1-\exp(-i(\omega-\omega_{10}) t))/(\omega_{10}-\omega))$

d. What is the probability of finding the system in $\ket1$ for all time?
> $c_1^1(t)=V_0/\hbar((1-\exp(+i\Sigma t))/\Sigma+(1-\exp(+i\Delta t))/\Delta)$
> $|c^1_1(t)|^2=V_0^2/\hbar^2|(1-e^{+i\Sigma t})/\Sigma+(1-e^{+i\Delta t})/\Delta|^2$
> $=V_0^2/\hbar^2((1-e^{+i\Sigma t})/\Sigma+(1-e^{+i\Delta t})/\Delta)((1-e^{-i\Sigma t})/\Sigma+(1-e^{-i\Delta t})/\Delta)$
> $=V_0^2/\hbar^2(((1-e^{+i\Sigma t})/\Sigma)((1-e^{-i\Sigma t})/\Sigma)+((1-e^{+i\Sigma t})/\Sigma)((1-e^{-i\Delta t})/\Delta))$
> $+V_0^2/\hbar^2(((1-e^{+i\Delta t})/\Delta)(1-e^{-i\Sigma t})/\Sigma+((1-e^{+i\Delta t})/\Delta)(1-e^{-i\Delta t})/\Delta))$
> $=V_0^2/\hbar^2(1-e^{+i\Sigma t})(1-e^{-i\Sigma t})/\Sigma^2)$
> $+V_0^2/\hbar^2(1-e^{+i\Sigma t})(1-e^{-i\Delta t})/\Delta\Sigma$
> $+V_0^2/\hbar^2(1-e^{+i\Delta t})(1-e^{-i\Sigma t})/\Sigma\Delta$
> $+V_0^2/\hbar^2(1-e^{+i\Delta t})(1-e^{-i\Delta t})/\Delta^2$
> $=V_0^2/\hbar^2(2-e^{+i\Sigma t}-e^{-i\Sigma t})/\Sigma^2)$
> $+V_0^2/\hbar^2(1-e^{+i\Sigma t}-e^{-i\Delta t}+e^{+i(\Sigma-\Delta)t})/\Delta\Sigma$
> $+V_0^2/\hbar^2(1-e^{+i\Delta t}-e^{-i\Sigma t}+e^{+i(\Delta-\Sigma)t})/\Sigma\Delta$
> $+V_0^2/\hbar^2(2-e^{+i\Delta t}-e^{-i\Delta t})/\Delta^2$
> $=V_0^2/\hbar^2(2-e^{+i\Sigma t}-e^{-i\Sigma t})/\Sigma^2)$
> $+V_0^2/\hbar^2(2-e^{+i\Sigma t}-e^{-i\Delta t}+e^{+i(\Sigma-\Delta)t}-e^{+i\Delta t}-e^{-i\Sigma t}+e^{+i(\Delta-\Sigma)t})/\Sigma\Delta$
> $+V_0^2/\hbar^2(2-e^{+i\Delta t}-e^{-i\Delta t})/\Delta^2$
> $=V_0^2/\hbar^2(2-2\cos\Sigma t)/\Sigma^2$
> $+V_0^2/\hbar^2(2-2\cos\Sigma t-2\cos\Delta t+2\cos(\Sigma-\Delta)t)/\Sigma\Delta$
> $+V_0^2/\hbar^2(2-2\cos\Delta t)/\Delta^2$
> $=V_0^2/\hbar^2(4\sin^2(\Sigma t/2))/\Sigma^2$
> $+V_0^2/\hbar^2(4\sin^2(\Delta t/2))/\Delta^2$
> $-V_0^2/\hbar^2(2-2\cos\Sigma t-2\cos\nabla t+2\cos(\Sigma+\nabla)t)/\Sigma\nabla$ ($\nabla=-\Delta$)
> $=4V_0^2/\hbar^2(\sin^2(\Sigma t/2)/\Sigma^2+\sin^2(\Delta t/2)/\Delta^2)$
> $+4V_0^2/\hbar^2(\sin(\Sigma t/2)\sin(\nabla t/2)\cos((\Sigma+\nabla)t/2))/\Sigma\nabla$
> $=4V_0^2/\hbar^2(\sin^2(\Sigma t/2)/\Sigma^2+\sin^2(\Delta t/2)/\Delta^2)$
> $+4V_0^2/\hbar^2(\sin(\Sigma t/2)\sin(\Delta t/2)\cos((\Sigma-\Delta)t/2))/\Sigma\Delta$

And we finally have:
> $=4V_0^2/\hbar^2(\sin^2(\Sigma t/2)/\Sigma^2+\sin^2(\Delta t/2)/\Delta^2-\sin(\Sigma t/2)\sin(\Delta t/2)\cos(\omega t))/\Sigma\Delta)$

Maybe. If the resonance frequency was around the frequency, then the $\Sigma$ in the denominator would be overshadowed leaving only:
> $(2V_0\sin(\Delta t/2)/\Delta\hbar)^2$

e. $c_1^{(1)}(t)$ represents the probabilities for going from a higher state to a lower state or vice versa. The slot that transitions from $\ket1\to\ket0$ represents giving up energy or stimulated emission, while the other takes energy to go from the ground state to a higher state or absorbing energy. 