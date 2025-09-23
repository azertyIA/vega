#EC455
E and H are *field intensity vectors*. D and B are *flux density vectors*.
> Electric: $\vec{D}=\epsilon\vec{E}$ (V/m)
> Magnetic: $\vec{B}=\mu\vec{H}$ (A/m)

Let's start with the Generalized Ampere's Law:
> $\nabla\times\vec{H}(\vec{r},t)=\vec{J_c}(\vec{r},t)+\partial_t\vec{D}(\vec{r},t)$

So why is one called conduction current ($\vec{J}_c$) while the other is called displacement current ($\partial_t\vec{D}$)? Both of them naturally have to have the same units (A/m2) but why are they called different things?

Let's start with the original Ampere's Law:
> $\nabla\times\vec{H}=\vec{J}_c$

You could actually see the magnetic current when you had just a DC battery, so people usually completely attributed magnetic fields to that. These concepts leak into other disciplines, so Maxwell saw it fit to make the equations complete. However the last term is invisible to DC batteries.

How did he get that equation then? The continuity equation, of course:
> $\partial_t\rho+\nabla\cdot\vec{J}=0$

In PY212, we might've not learned about this displacement current, but we have learned about capacitors: there's an insulator between the two ends of the capacitor. In DC, it makes sense: no moving charges, no magnetic field. However, in AC, something else occurs:

Every half time frequency, the E field will change directions. So, still no $\vec{J}_c$ occurs across the dielectric, but the $\vec{E}$ field is constantly changing.
> $\nabla\times\vec{H}=\epsilon\partial_t\vec{E}$, where $\epsilon$ is the physical property of the dielectric permittivity.

But how did we get there? Again?

Let's start with the original Ampere's Law:
> $\nabla\times\vec{H}=\vec{J}_c$
> $\nabla\cdot(\nabla\times\vec{H})=\nabla\cdot\vec{J}_c=0$

But what else could we put there to ensure that the divergence of the curl is 0? The answer lies in the continuity equation:
> $\nabla\cdot(\nabla\times\vec{H})=\nabla\cdot\vec{J}_c+\partial_t\rho=0$
> $=\nabla\cdot\vec{J}_c+\nabla\cdot\partial_t\vec{D}$ (Gauss Law)
> $=\nabla\cdot(\vec{J}_c+\partial_t\vec{D})$

The continuity equation perfectly introduces a time-derivative term that gets eliminated in DC situations. Meanwhile, we put this entire thing into the divergence of a curl property to get the intersection of these two properties.

Moving on, a monochromatic signal represents a sinusoidal with one frequency and an amplitude:
> $\hat{e}E_0\cos(\omega{t}+\phi)=\vec{E}(\vec{r},t)=\Re{\vec{E}(\vec{r})e^{j\omega{t}}}$

Time averages are important because you get more of a general picture through averages in AC steady states than instantaneous forms. The general form uses:
> $\braket{E(\vec{r},t)}_T=\frac{1}{T}\int dtE(\vec{r},t)=\vec{E}(\vec{r})$

Using this naively leads you to get that the time average of a sinusoidal ends up being zero. So what can we do? Just square the sinusoidal and root it after:
> $\sqrt{\braket{E(\vec{r},t)^2}_T}=\frac{1}{\sqrt{T}}\sqrt{\int dtE(\vec{r},t)^2}$
> $=\frac{\hat{e}E_0}{\sqrt{T}}\sqrt{\int dt\cos(\omega t+\phi)^2}$
> $=\frac{\hat{e}E_0}{\sqrt{\omega T}}\sqrt{\int du\cos^2u}$
> $=\frac{\hat{e}E_0}{\sqrt{2\omega T}}\sqrt{\int du(1+\cos2u)}$
> $=\frac{\hat{e}E_0}{\sqrt{2}}$

Let's move onto Faraday's law stuff. Consider a circuit loop with two resistors ($3,7 k\Omega$) If there is a current, then there is a magnetic field. Or vice versa. This is basically a solenoid with one turn. We can sense changes of magnetic field using this and measuring the voltage across one of the resistors.