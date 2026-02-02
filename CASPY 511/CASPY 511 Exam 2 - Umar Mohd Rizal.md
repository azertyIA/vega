I have decided to do LaTeX this time around.
## Q1. Momentum Space Wavefunction (6 points)
Consider the Harmonic oscillator in 1D of a non-relativistic particle of mass m attached to the origin by a spring. Plot the probability density associated with the first excited state momentum- space wavefunctions. 
> $\braket{k|1}=\int dx\exp[-ikx]\braket{x|1}$
> $=\int dx\exp[-m\omega_0x^2/2\hbar-ikx](\frac{m\omega_0}{\pi\hbar})^{1/4}\sqrt{\frac{2m\omega_0}\hbar}x$
> $=(\frac{m\omega_0}{\pi\hbar})^{1/4}\sqrt{\frac{2m\omega_0}\hbar}\int dxx\exp[-m\omega_0x^2/2\hbar-ikx]$ (plug into Mathematica)
![[Pasted image 20251121210242.png]]
> $=-2i\pi^{1/4}(\hbar/m\omega)^{3/4}k\exp[-\hbar k^2/2m\omega]$
> $\boxed{|\braket{k|1}|^2=4\sqrt{\pi\hbar^3/m^3\omega^3}k^2\exp[-\hbar k^2/m\omega]}$ (total probability is $2\pi$)

![[Pasted image 20251121215309.png]]`
*A depiction of the probability density of a given momentum, note the two bumps indicating that the particle is more likely to be moving in either direction over being still. Do make note of the obscure scaling to put it in SI units. The scale magnitude is based on the square root of Planck's reduced constant.*
## Q2. Interaction Potential (6 points)
For a familiar SHO, try to find the interaction potential in terms of the time, position and momentum operators as well as the given parameters intrinsic to the SHO.
> $\hat H=\hat H_0+V(\hat x)=\frac1{2m}\hat p^2+\frac12m\omega^2_0\hat x^2$
> $V_I=e^{+i\hat H_0t/\hbar}V(\hat x)e^{-i\hat H_0t/\hbar}$
> $=e^{+i\hat H_0t/\hbar}(\frac12m\omega_0^2\hat x^2)e^{-i\hat H_0t/\hbar}$
> $=\frac12m\omega_0^2e^{+i\hat H_0t/\hbar}(\hat x^2)e^{-i\hat H_0t/\hbar}$
> $=\frac12m\omega_0^2e^{\hat A}(\hat x^2)e^{-\hat A}$ ($\hat A=i\hat p^2t/2\hbar m$)

Before continuing let's first examine the commutator $[\hat p^2,\hat x^2]$:
> $=\hat p[\hat p,\hat x^2]+[\hat p,\hat x^2]\hat p$
> $=\hat p(\hat x[\hat p,\hat x]+[\hat p,\hat x]\hat x)+(\hat x[\hat p,\hat x]+[\hat p,\hat x]\hat x)\hat p$
> $=-i\hbar(2\hat p\hat x+2\hat x\hat p)$
> $=-2i\hbar(\hat p\hat x+\hat x\hat p)$
> $=-2i\hbar(2\hat p\hat x+\hat x\hat p-\hat p\hat x)$
> $=-2i\hbar(2\hat p\hat x+i\hbar)$
> $=-4i\hbar\hat p\hat x+2\hbar^2$

And again with $[\hat p^2,\hat p\hat x]$:
> $=\hat p[\hat p^2,\hat x]+[\hat p^2,\hat p]\hat x$
> $=2\hat p^2[\hat p,\hat x]$
> $=-2i\hbar\hat p^2$ (which definitely commutates with $\hat A$)

Returning back:
> $=\frac12m\omega_0^2(\hat x^2+[\hat A,\hat x^2]+\frac12[\hat A[\hat A,\hat x^2]]+0)$
> $=\frac12m\omega_0^2(\hat x^2+(it/2\hbar m)[\hat p^2,\hat x^2]+(-t^2/8\hbar^2 m^2)[\hat p^2[\hat p^2,\hat x^2]]+0)$
> $=\frac12m\omega_0^2(\hat x^2+(it/2\hbar m)[-4i\hbar\hat p\hat x+2\hbar^2]+(-t^2/8\hbar^2 m^2)[\hat p^2,-4i\hbar\hat p\hat x]+0)$
> $=\frac12m\omega_0^2(\hat x^2+(t/m)[2\hat p\hat x+i\hbar]+(i t^2/2\hbar m^2)[\hat p^2,\hat p\hat x])$
> $=\frac12m\omega_0^2(\hat x^2+(t/m)[2\hat p\hat x+i\hbar]+(i t^2/2\hbar m^2)[-2i\hbar\hat p^2])$
> $=\frac12m\omega_0^2(\hat x^2+(t/m)[2\hat p\hat x+i\hbar]+(t^2/ m^2)[\hat p^2])$
> $=\frac12m\omega_0^2(\hat x^2+(t/m)[\hat p\hat x+\hat x\hat p]+(t^2/ m^2)[\hat p^2])$
> $\boxed{=\frac12m\omega_0^2(\hat x+\hat pt/m)^2}$
## Q3. Josephson-Junction (6 points)
Consider Feynman's two-state model of the Josephson Junction and one of the Josephson equations (you only need one for this problem...):
> $\partial_t(\phi_2-\phi_1)=\partial_t\Delta\phi=2eV/\hbar$
> and given $V(t)=(\hbar\omega/2e)\cos\omega t$

Find an expression for the Josephson current $I(t)=I_c\sin(\Delta\phi)$
> $(\Delta\phi)(t)-(\Delta\phi)(0)=(2e/\hbar)\int dtV(t)$
> $=(2e/\hbar)(\hbar\omega/2e)\int dt\cos\omega t$
> $=\sin\omega t$
> $\boxed{I(t)=\sin(\phi_0+\sin\omega t)}$

Is there a DC current?
> It depends on the initial phase difference between the two states. The closer the two phases are to being perfectly opposite or perfectly matching, the closer the DC point gets to zero. The closer $\sin\phi_0$ is to its minimum or maximum, there will be a matching DC voltage on that side. Meanwhile, the inner sin function truly drives the periodicity around the DC point.

![[Pasted image 20251122030102.png]]
*Three different graphs for three different solutions to the initial value problem (phase difference between the two states). I kept omega at 1 Hz because it doesn't change anything fundamental about the system. The trends in changes in DC led me to create the next graph.*
![[Pasted image 20251122030112.png]]
*This graph has the phase difference on the x-axis and the DC voltage (I just found the mean of the period) on the Y axis. notice how the maximum occurs near $\pi/2$ and the minimum at $3\pi/2$.*
## Q4. Displacement Operator (6 points)
Which of the following correctly turns coherent state $\ket\alpha\to\ket\beta$?
> $\hat D(\alpha)\ket\gamma=\ket{\alpha+\gamma}$
> $\hat D(\alpha)^\dagger=(e^{\alpha^*\hat a-\alpha\hat a^\dagger})^\dagger=\hat D(-\alpha)$
> $\hat D(\alpha)+\hat D(\beta)=\hat D(\alpha+\beta)$ (not accounting for phase)
> $\hat D(\alpha-\beta)\ket\alpha=\ket\beta$ (not accounting for phase)

Now let's look at the students' answers.
> Alfie: $\hat D(-\beta)\hat D(-\alpha)=\hat D(-\beta-\alpha)$
> Betty: $\hat D(\beta)\hat D^\dagger(\alpha)=\hat D(\beta-\alpha)$
> Gammy: $\hat D(\beta)\hat D(\alpha)=\hat D(\beta+\alpha)$
> Delter: $\hat D^\dagger(-\beta)\hat D^\dagger(\alpha)=\hat D(\beta-\alpha)$
> Epsom: $\hat D^\dagger(\alpha)\hat D^\dagger(\beta)=\hat D(-\beta-\alpha)$
> **Only Delter and Betty are right and deserve full credit.**
## Q5. Quantum LC Circuit (6 points)
Consider the quantized LC circuit with a linear inductor and capacitor in parallel. You are given that the inductance $L=10\text{nH}$ and that the resonance frequency $\omega=5\text{GHz}$.

a. What is the capacitance $C$?
> $C=1/L\omega^2$
> $=(1/250\times10^9)(\text{s}^2\text{/H})$
> $=(4/1000\times10^9)F$
> $=4\text{pF}$

b. Is this circuit useful in detecting a change in charge stored across the capacitor associated with a single Cooper pair?
> The "energy" (I know my voltages better) it takes to store such a pair would be $V=Q/C$
> $\approx(2*10^{-19}C/4*10^{-12}F)=50nV<<k_BT/e=25mV$ at room temperature and would still be hard to measure in controlled sub-Kelvin environments. The difference in magnitude would sweep away any hope at detecting a cooper pair. An even smaller capacitance is required.

c. Is this circuit capable of simultaneously detecting a single flux quantum?
> No. Detecting flux quanta means discrete states need to be discernable, but we would never know what state it's in because the linearity of the inductor and capacitor create a perfectly harmonic oscillator. As a result, the energy levels between states are the same and we cannot capture such a state to gather that kind of information, unlike in an anharmonic oscillator (JJ).
## L1. Momentum Perturbation (10 points)
A SHO in 1D is subject to a weak momentum-dependent constant $V_1=\lambda\hat p$:
> $\hat H=\hat p^2/2m+\frac12m\omega^2_0\hat x^2+\lambda\hat p$

a. What are the dimensions of $\lambda$? Write down a condition for which the perturbation may be considered "weak."
> $\boxed{\lambda=\text{energy}/\text{momentum}=\text{velocity}=\text{distance}/\text{time}}$
> We want $\lambda\braket\hat p<<\frac12\hbar\omega$ (ground state) and LHS is proportional to some form of $\Delta_p\propto\sqrt{\hbar\omega m}$, so it's safe to say that $\boxed{\lambda<<\sqrt{\hbar\omega/m}}$ leads to a weak perturbation.

b. Show that the Hamiltonian can be rewritten as $\hat H=\frac12\hat P^2+\frac12\hat X^2+\text{constant}$:
> $\hat H=\hat p^2/2m+\lambda\hat p+\frac12m\omega^2_0\hat x^2$
> $=\hat p^2/2m+\lambda\hat p+\lambda^2m/2-\lambda^2m/2+\frac12m\omega^2_0\hat x^2$
> $=\frac12(\hat p^2/m+\lambda\hat p+\lambda^2m)-\lambda^2m/2+\frac12m\omega^2_0\hat x^2$
> $=\boxed{\frac12(\hat p/\sqrt m+\lambda\sqrt m)^2+\frac12(\sqrt m\omega_0\hat x)^2-\lambda^2m/2}$
> $\hat P=\hat p/\sqrt m+\lambda\sqrt m$
> $\hat X=\sqrt m\omega_0\hat x$
> $\text{constant}=-\lambda^2m/2$
	
c. What is the commutator $[\hat X,\hat P]?$
> $=[\sqrt m\omega_0\hat x,\hat p/\sqrt m]$ (constant disappear)
> $=\omega_0[\hat x,\hat p]$
> $=\boxed{i\hbar\omega_0}$

d. Going back to the original Hamiltonian, find the correction to the first excited state energy of the unperturbed oscillator state $\ket1$ due to the perturbation $\hat V_1=\lambda\hat p$.
> Looking at b, it should rely on the constant term $-\lambda^2m/2$ meaning less energy than the original oscillator. Taking a first order Dyson series would neglect this result.
> $\boxed{E_1=\frac32\hbar\omega_0-\lambda^2m/2}$ 
## L2. Landau Levels, Symmetric Gauge (10 points)
Given the following symmetric gauge from Sakurai for a rectangular plate:
> $\vec A=\braket{-\frac12B_0y,\frac12B_0x,0}$

a. Check that this gauge produces a uniform magnetic field $\vec B=B_0\hat z$:
> $\vec B=\nabla\times\vec A$
> $=\nabla\times\braket{-\frac12B_0y,\frac12B_0x,0}$
> $=\frac12\braket{0,0,\partial_x(B_0x)-\partial_y(-B_0y)}$
> $=\frac12\braket{0,0,2B_0}$
> $=\boxed{\braket{0,0,B_0}=B_0\hat z}$

b. Set up the 2D Hamiltonian and show that the TISE resembles a 2D QHO:
> $\partial_t\Lambda(\vec x,t)=\partial_t\Lambda(\vec x)=0$
> $\partial_t\Phi(\vec x,t)=\partial_t\Phi(\vec x)=0$
> $\hat H=\frac1{2m}(\vec p-q\vec A)^2+q\Phi$

In terms of the position basis:
>$E\braket{\vec x|\Psi}=[\frac1{2m}(-i\hbar\nabla-q\vec A)^2+q\Phi]\braket{x|\Psi}$
>$=[\frac1{2m}(-i\hbar\braket{\partial_x,\partial_y,\partial_z}-q\braket{-\frac12B_0y,\frac12B_0x,0})^2+q\Phi]\braket{\vec x|\Psi}$
>$=[\frac1{2m}(-i\hbar\braket{\partial_x,\partial_y,0}-q\braket{-\frac12B_0y,\frac12B_0x,0})^2+q\Phi]\braket{\vec x|\Psi}$ (no z-dependence)
>$=[\frac1{2m}(\braket{-i\hbar\partial_x-\frac12qB_0y,-i\hbar\partial_y+\frac12qB_0x,0})^2+q\Phi]\braket{\vec x|\Psi}$
>$=[\frac1{2m}((-i\hbar\partial_x-\frac12qB_0y)^2+(-i\hbar\partial_y+\frac12qB_0x)^2)]\braket{\vec x|\Psi}$ (luckily $\partial_x$ commutes with $y$)
>$=[\frac1{2m}(-\hbar^2\partial_x^2+i\hbar qB_0y\partial_x+\frac14q^2B_0^2y^2-\hbar^2\partial_y^2-i\hbar qB_0x\partial_y+\frac14q^2B_0^2x^2)]\braket{\vec x|\Psi}$
>$=[\frac1{2m}(-\hbar^2\partial_x^2-\hbar^2\partial_y^2+i\hbar qB_0y\partial_x-i\hbar qB_0x\partial_y+\frac14q^2B_0^2y^2+\frac14q^2B_0^2x^2)]\braket{\vec x|\Psi}$
>$=[\frac1{2m}(-\hbar^2\nabla^2-i\hbar qB_0(x\partial_y-y\partial_x)+\frac14q^2B_0^2(x^2+y^2)]\braket{\vec x|\Psi}$
>$\boxed{\hat H=\frac1{2m}(\vec p^2-qB_0\hat L_z+\frac14q^2B_0^2\vec x^2)}$ (Sakurai's angular momentum operator)

c. Re-write the Schrodinger equation in terms of polar coordinates in 2D.
> $x=r\cos\phi\to dx=dr\cos\phi-rd\phi\sin\phi$
> $y=r\sin\phi\to dy=dr\sin\phi+rd\phi\cos\phi$
> Linear system, so invert to find other differentials (Jacobian)

``` 
(i usually use this block for linalg scratch work, latex isnt fun)

dx = + cos p  -rsin p | dr
dy = + sin p  +rcos p | dp

dr = + cos p  + sin p | dx
dp = -Rsin p  +Rcos p | dy (R=1/r)
```

> $\partial_xr=\cos\phi,\partial_yr=\sin\phi$
> $\partial_x\phi=-\sin\phi/r,\partial_y\phi=\cos\phi/r$

> $\partial_x=(\partial_xr)\partial_r+(\partial_x\phi)\partial_\phi=\cos\phi\partial_r-\frac1r\sin\phi\partial_\phi$
> $\partial_y=(\partial_yr)\partial_r+(\partial_y\phi)\partial_\phi=\sin\phi\partial_r+\frac1r\cos\phi\partial_\phi$
> $\nabla^2=\partial_x^2+\partial_y^2=\partial_r^2+\frac1{r^2}\partial_\phi^2+\frac1r(\cos^2\phi+\sin^2\phi)\partial_r$
> $=\partial_r^2+\frac1r\partial_r+\frac1{r^2}\partial_\phi^2$

> $x\partial_y-y\partial_x$
> $=\cos\phi(r\sin\phi\partial_r+\cos\phi\partial_\phi)-\sin\phi(r\cos\phi\partial_r-\sin\phi\partial_\phi)$
> $=\cos^2\phi\partial_\phi+\sin^2\phi\partial_\phi$
> $=\partial_\phi$

Going back to our dear Hamiltonian:
>$[\frac1{2m}(-\hbar^2(\partial_r^2+\frac1r\partial_r+\frac1{r^2}\partial_\phi^2)-i\hbar qB_0(2r\cos\phi\sin\phi\partial_r+(\cos^2\phi-\sin^2\phi)\partial_\phi)+\frac14q^2B_0^2r^2]\braket{\vec x|\Psi}$
>$=\boxed{[\frac1{2m}(-\hbar^2(\partial_r^2+\frac1r\partial_r+\frac1{r^2}\partial_\phi^2)-i\hbar qB_0\partial_\phi+\frac14q^2B_0^2r^2]\braket{\vec x|\Psi}}$

d. Is there a degeneracy associated with the ground state?
> Given a uniform magnetic field, it doesn't matter where the center of this oscillator cyclotron thing is, it's still going to have the same energy, so there's infinitely many degenerate states across the continuous area of the metal square.

## Code for Quickies Appendix
Q1
```
import numpy as np
import matplotlib.pyplot as plt

obscure_scaling = 10 ** -34
h_bar = 1.054 * obscure_scaling # J-s
mass = 1 # kg
omega = 1 # Hz
factor = h_bar / mass / omega

def psi2_p(p):
    return 4 * (np.pi * factor ** 3) ** 0.5 * (p / h_bar) ** 2 * np.exp(-factor * (p / h_bar) ** 2)

ps = np.linspace(-5,5,1000) * obscure_scaling ** 0.5
plt.plot(ps, psi2_p(ps))
plt.title("Probability Density of Momentum")
plt.ylabel("|<p|1>|²")
plt.xlabel("p=ℏk (kg-m/s)")
```
Q3
```
import numpy as np
import matplotlib.pyplot as plt

omega = 1 # Hz
phi = 0
ps = np.linspace(0,np.pi * 2,1000)
ts = np.linspace(0,np.pi * 2,1000)
s = 5

fig, (ax1,ax2,ax3) = plt.subplots(3,1)
fig.set_size_inches(8,8)

def f(t,phi):
    return np.sin(phi + 0.4 * np.sin(omega * t))

ts = np.linspace(0,5,1000) * s
ax1.set_title("AC Voltage: Josephson Current over Time")
ax1.plot(ts, f(ts,0))
ax1.plot(ts, f(ts,0).mean() + 0 * ts)
ax1.set_ylabel("Current (Ic) dPhi=0rad")
ax2.plot(ts, f(ts,1))
ax2.plot(ts, f(ts,1).mean() + 0 * ts)
ax2.set_ylabel("Current (Ic) dPhi=1rad")
ax3.plot(ts, f(ts,2))
ax3.plot(ts, f(ts,2).mean() + 0 * ts)
ax3.set_ylabel("Current (Ic) dPhi=2rad")
plt.xlabel("Time (s)")
```
```
import numpy as np
import matplotlib.pyplot as plt

omega = s # Hz
ps = np.linspace(0,np.pi * 2,200)
ts = np.linspace(0,np.pi * 2,200)

def f(t,phi):
    return np.sin(phi + np.sin(omega * t))

ms = [np.array([f(t,p) for t in ts]).mean() for p in ps]

plt.plot(ps * 180 / np.pi, ms)
plt.title("AC Voltage: Josephson DC Phase Analysis")
plt.ylabel("Current (Ic)")
plt.xlabel("Phase Difference (deg)")
```