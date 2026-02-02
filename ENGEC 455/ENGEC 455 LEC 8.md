In high school chemistry, we learned about polarization. Also in 511 apparently.

An electric dipole moment features a distance and a charge differential. So it's like a capacitor. WBUR is like a point source. You are typically a **stationary** observer. Imagine a field vector. 

If the electric field is linearly polarized then the electric field only moves about a line. If the electric field traces out a circle, then it's circularly polarized. Otherwise it's probably elliptically polarized. It should be clockwise or counter clockwise.

If two components are in phase then they are linear. If the phase is orthogonal then it's circular. Otherwise it's elliptical

You have to turn these phasor forms into instantaneous time-domain phenomenon by multiplying by $\exp j\omega t$, and taking the real component.

> $\Re[\hat xE_{10}e^{j(\omega t-kz)}+\hat yE_{20}e^{j(\omega t - kz+\pi/2)}]$
> $\hat xE_{10}\cos(\omega t-kz)-\hat yE_{20}\sin(\omega t - kz)$

If we wanted to see how it evolved in time just sit on the origin and z = 0. Then just take two timesteps at $\omega t=0$ and $\omega t=\pi/2$.

So what does a complex wavenumber mean? Take the following waveform:
> $\vec E=\hat xE_0e^{j(\omega t-kx)}$

Think about a microwave. You don't need that power much to cook food. But it does operate in gigahertz. The imaginary component leads to a real exponential growth or decay. Usually it's bad if something leads to exponential growth. You can similarly set $t=0$ and see how the wave evolves across space.