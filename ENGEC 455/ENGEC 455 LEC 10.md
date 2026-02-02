The power flux will be used to cook food. So, how can we increase the efficiency? A magneton can be used for many cases. For instance, the microwave. The wavelength of BU radio station is about 3 meters.

Now we have the Poynting vector: 
> $\vec P(\vec r,t)=\vec E\times\vec H$

E goes on x, H goes on y, and the Poynting vector goes on the z ($\hat k$). Thus the power flux can be used:
> $\oint_Sd\vec s\cdot\vec P=\iiint dV(\nabla\cdot\vec P)$
> $=\iiint dV(\nabla\cdot(\vec E\times\vec H))$
> $=\iiint dV(\vec H\cdot\nabla\times\vec E-\vec E\cdot\nabla\times\vec H)$
> $=\iiint dV(\vec H\cdot(\nabla\times\vec E)-\vec E\cdot(\nabla\times\vec H))$
> $=\iiint dV(-\vec H\cdot(\mu_0\partial_t\vec H)-\vec E\cdot(\vec J+\epsilon_0\partial_t\vec E))$
> $=-\iiint dV(\vec H\cdot(\mu_0\partial_t\vec H)+\vec E\cdot(\vec J+\epsilon_0\partial_t\vec E))$
> $=-\iiint dV(\vec H\cdot(\mu_0\partial_t\vec H)+\vec E\cdot((\sigma+\epsilon_0\partial_t)\vec E))$
> $=-\iiint dV(\frac{\mu_0}2\partial_tH^2+\frac{\epsilon_0}2\partial_tE^2+\sigma E^2)$
> $=-\partial_t\iiint dV(\frac{\mu_0}2H^2+\frac{\epsilon_0}2E^2)-\iiint dV\sigma E^2$

Get rid of the $0$ in the constants and it's super generalized. Non generalized:
> $=-\iiint dV(\vec H\cdot(j\mu_0\omega\vec H)+\vec E\cdot((\sigma+j\epsilon_0\omega)\vec E))$
> $=-\iiint dV(j\mu_0\omega H^2+(\sigma+j\epsilon_0\omega)E^2)$

If we look at the two terms in the first integral of the generalized version, then you get magnetic and electric energy density, while the second integral represents ohmic heating. 

The two energy densities are supposed to be equal.
> $E^2=\eta^2H^2=\frac\mu\epsilon H^2$ (it was eta this whole time??????????

Imagine a DC wire.
> $\vec I=\vec J_cS=\sigma\vec ES$
> $\vec I/\sigma S=\vec E=\hat zE$

The maximum magnetic field is:
> $H=I/2\pi r_0=\sigma ES/2\pi r_0$

I lowkey forgot how right hand rule works. But $E\times H$ ends up being inward always.
> $\vec P=\hat zE\times I/2\pi r_0\hat\phi=-\hat r E(\sigma ES)/2\pi r_0$
> $\vec s=\hat r(2\pi r_0L)$
> $\oint_Sd\vec s\cdot\vec P=(-\hat r\cdot\hat r)\sigma E^2(\pi r_0^2)L$
> $=-\sigma E^2(\pi r_0^2)L$

Yo brain farting dawg:
> $R=\frac L{\sigma A}=\frac L{\sigma(\pi r_0^2)}$
> $\oint d\vec s\cdot\vec P=-RI^2=-V^2/R$

Now let's take the time average for this power, assume they are in phase.
> $\vec P_{avg}(\vec r)=\frac1T\int dt\vec P(\vec r,t)$
> $\vec P_{avg}(\vec r)=\frac1T\int dt\vec P(\vec r,t)$