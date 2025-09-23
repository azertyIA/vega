Let's start with Maxwell's equations for today (half scalars, half vectors):
> $\nabla\cdot\vec{D}=\rho_v$
> $\nabla\cdot\vec{B}=0$
> $\nabla\times\vec{E}=-\partial_t\vec{B}$
> $\nabla\times\vec{H}=\vec{J_c}+\partial_t\vec{D}$
> $\partial_t\rho_v=\nabla\cdot\vec{J_c}=0$

E and H are *field intensity vectors*. D and B are *flux density vectors*.
> Electric: $\vec{D}=\epsilon\vec{E}$ (V/m)
> Magnetic: $\vec{B}=\mu\vec{H}$ (A/m)

The continuity equation notes the sources for electric and magnetic fields. There is no need for a magnetic charge.

Moving on to other theorems, Divergence Theorem deals with closed surfaces while Stoke's Theorem deals with open surfaces:
> Divergence Theorem: $\int_VdV(\nabla\cdot\vec{D})=\oint_Sd\vec{s}\cdot\vec{D}$
> Stoke's Theorem: $\int_SdS\cdot(\nabla\times\vec{D})\oint_r=\oint_rd\vec{l}\cdot\vec{D}$

Electric fields have units *volts per meter* while magnetic fields have units *amps per meter*.

You can use dimensional analysis to sanity check for understanding. For example, the two terms in the last Maxwell Equation both have the same units. Speaking of units, the most internationally favored unit system is MKS (meters-kilogram-second). 

(But meters are defined by light-seconds anyways.)

MKS creates a few units of its own:
> Force = K-M/S2 (Newton)
> Energy = K-M2/S2 (Joules)
> Power = K-M2/S3 (Watts)

Going back to this relation, we need this to define some physical constants (in vacuum):
> $\vec{D}=\epsilon\vec{E},\vec{B}=\mu\vec{H}$

We can use these physical constants to create a very important constant:
> $c=\frac{1}{\sqrt{\mu_0\epsilon_0}},\mu_0=4\pi\times10^{-7}$

Now that we're moving to phasors, the one condition we need is AC steady-state or sinusoidal most of the time.

Let's take the example of RC circuits for example. Trying to solve for voltage in DC (or $\omega=0$), you get a exponential decay (transient) term and a non-functional term:
> $V(t)=V_0e^{-t/RC}+V_{AC}$

Allegedly we don't care about transient processes because usually it means disaster, so we should care more about the steady-states. Because KVL is a linear system, you can use superposition on nearly anything. So, these steady-states and transient process just need to add to make your true answer.

Let's talk about some passive components:
> Resistors: $V_R=IR$
> Capacitors: $I_C=C\partial_tV$
> Inductors: $V_L=L\partial_tI$

The phasor form is the following frequency of three parameters ($A,\omega,\phi$):
> $V_{AC}=V_0\cos(\omega t+\phi)=\Re V_0e^{j(\omega t+\phi)}=\Re V_se^{j\omega t}$

Where $V_s$ is the phasor form. When you take the real component, you get the instantaneous form.