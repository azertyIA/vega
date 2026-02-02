## 4.1. Pencil Boohoo

The neutrino flavor =/= neutrino mass
> $\begin{pmatrix}\nu_e\\\nu_\mu\end{pmatrix}=R(\theta)\begin{pmatrix}\nu_1\\\nu_2\end{pmatrix}$
> $\ket e,\ket\mu,\ket1,\ket2$
> $H_0\ket1=E_1\ket1$
> $H_0\ket2=E_2\ket2$
> $\ket e=\cos\theta\ket1-\sin\theta\ket2$
> $\ket\mu=\sin\theta\ket1+\cos\theta\ket2$

$P(e\to e)=|\bra eU(t,t_0)\ket e|^2$ 
> $\bra eU(t,t_0)\ket e$ 
> $\bra e e^{iH_0t/\hbar}\ket e$ 
>$\bra e e^{iH_0t/\hbar}(\cos\theta\ket1-\sin\theta\ket2)$ 
> $\bra e (e^{-iE_1t/\hbar}\cos\theta\ket1-e^{-iE_2t/\hbar}\sin\theta\ket2)$ 
> $(\cos\theta\bra1-\sin\theta\bra2)(e^{-iE_1t/\hbar}\cos\theta\ket1-e^{-iE_2t/\hbar}\sin\theta\ket2)$ 
> $(\cos^2\theta e^{-iE_1t/\hbar}+\sin^2\theta e^{-iE_2t/\hbar})$
> $e^{-iE_1t/\hbar}(\cos^2\theta +e^{-i\Delta Et/\hbar}\sin^2\theta)$

> $|\bra eU(t,t_0)\ket e|^2$ 
> $|(\cos^2\theta +e^{-i\Delta Et/\hbar}\sin^2\theta)|^2$ 
> $(\cos^2\theta +e^{-i\Delta Et/\hbar}\sin^2\theta)(\cos^2\theta +e^{+i\Delta Et/\hbar}\sin^2\theta)$ 
> $=\cos^2\theta(\cos^2\theta +e^{+i\Delta Et/\hbar}\sin^2\theta)$
> $+e^{-i\Delta Et/\hbar}\sin^2\theta(\cos^2\theta +e^{+i\Delta Et/\hbar}\sin^2\theta)$ 
> $=\cos^4\theta+\cos^2\theta \sin^2\theta e^{+i\Delta Et/\hbar}$
> $+e^{-i\Delta Et/\hbar}\sin^2\theta\cos^2\theta +\sin^4\theta$ 
> $=1-2\cos^2\theta \sin^2\theta (1-\cos\Delta Et/\hbar)$
> $=1-2\cos^2\theta \sin^2\theta (2\sin^2\Delta Et/2\hbar)$
> $=1-\sin^22\theta\sin^2\Delta Et/2\hbar$

> $E=\sqrt{p^2c^2+m^2c^4}$
> $=pc\sqrt{1+m^2c^2/p^2}$
> $=pc(1+m^2c^2/2p^2)$
> $=pc+m^2c^3/2p$

> $\Delta E=pc-pc+\Delta(m^2)c^3/2p$
> $=\Delta(m^2)c^3/2p$
> $=\Delta m^2c^4/2E$

> $1-\sin^22\theta\sin^2\Delta Et/2\hbar$
> $1-\sin^22\theta\sin^2\Delta m^2c^4t/4E\hbar$
> $1-\sin^22\theta\sin^2\Delta m^2c^4L/4E\hbar c$
## 4.2. Rabi Flopping

The Hamiltonian is the following:
> $H=\begin{pmatrix}\epsilon_0&\gamma e^{-i\chi}\\\gamma e^{+i\chi}&\epsilon_1\end{pmatrix}$. 

## 4.4. Harmonic Oscillators

> $\hat H_x=-\frac{\hat p^2}{2m}+\frac{1}{2}k\hat x^2$
> $\hat H_x=-\frac{\hbar^2}{2m}\partial^2_x+\frac{1}{2}m\omega^2x^2$ 
> $\hat H_y=-\frac{\hbar^2}{2m}\partial^2_y+\frac{1}{2}m\omega^2y^2$

Adding the two:
> $\hat H_x+\hat H_y=-\frac{\hbar^2}{2m}(\partial^2_x+\partial^2_y)+\frac{1}{2}m\omega^2(x^2+y^2)$
> $\hat H_x+\hat H_y=-\frac{\hbar^2}{2m}(\nabla\cdot\nabla)+\frac{1}{2}m\omega^2(x^2+y^2)$
> $\hat H_x+\hat H_y=-\frac{\hbar^2}{2m}\nabla^2+\frac{1}{2}m\omega^2(x^2+y^2)$

Defining energy states:
> $E_x=\hbar\omega_0(n_x+\frac12)$
> $E_y=\hbar\omega_0(n_y+\frac12)$

There are $N+1$ possible ways to make $N$.

Ladder operators:
> $\hat a=\sqrt{m\omega_0/2\hbar}(x+ip/m\omega_0)$ (annihilation)
> $\hat a=\sqrt{1/2\hbar m\omega_0}(m\omega_0x+ip)$ (annihilation)
> $\hat a^\dagger=\sqrt{m\omega_0/2\hbar}(x-ip/m\omega_0)$ (creation)

Position:
> $\hat x=\Delta_x(\hat a_x+\hat a_x^\dagger)$
> $\hat x=\Delta_x\sqrt{m\omega_0/2\hbar}(2\hat x)$
> $\hat x=\Delta_x\sqrt{2m\omega_0/\hbar}(\hat x)$
> $1=\Delta_x\sqrt{2m\omega_0/\hbar}$
> $\Delta_x=\sqrt{\hbar/2m\omega_0}$

Momentum:
> $\hat p=\Delta_p()$


