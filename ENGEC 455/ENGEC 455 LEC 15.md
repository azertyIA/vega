For a TM wave, ($H_z=0$, $E_z\neq0$)*
> *$0=(\nabla^2+k^2)\mathbb E$*
> *$=(\partial_y^2+\gamma^2+k^2)E_z$*
> *$=(\partial_y^2+h^2)E_z$*
> *where $h=n\pi/d$*

*It may seem hard to solve five more equations, but the E and H fields are a lot more dependent on each other than it seems. For instance, Faraday's law and Generalized Ampere's Law help combine the two ideas:*
> *Faraday's Law: $\nabla\times\vec E=-\mu\partial_t\vec H=-j\omega\mu\vec H$*
> *Ampere's Law: $\nabla\times\vec H=\epsilon\partial_t\vec E=j\omega\epsilon\vec E$*

*In general the equation of $(\nabla^2+1/\lambda)E_z=0$ can expand to:*
> *$H_x=-\lambda(\gamma\partial_xH_z-j\omega\epsilon\partial_yE_z)$*
> *$H_y=-\lambda(\gamma\partial_yH_z+j\omega\epsilon\partial_xE_z)$*
> *$E_x=-\lambda(\gamma\partial_xE_z+j\omega\mu\partial_yH_z)$*
> *$E_y=-\lambda(\gamma\partial_yE_z-j\omega\mu\partial_xH_z)$*

For TEM, these should all be zero right? But how is that possible? We can assume that $1/\lambda=0$. As long as both the numerator and the denominator approach zero of infinity in some way. In our case, both should approach zero. The wave number $k$ must be a real number, so $\gamma$ must be a fully imaginary number.
> $\gamma=\pm jk$
> $\psi_{TEM}=Ae^{-jkz}+Be^{+jkz}$

Going back to TM waves:
> $H_x=j\lambda\omega\epsilon\partial_yE_z$
> $H_y=-j\lambda\omega\epsilon\partial_xE_z$
> $E_x=-\lambda\gamma\partial_xE_z$
> $E_y=-\lambda\gamma\partial_yE_z$

If $\gamma=0$, then your wave function goes to zero, Or a wave that kind of doesn't exist.
> $0=\gamma^2=h^2-k^2$
> $=(n\pi/d)^2-(\omega/c)^2$
> $\omega=cn\pi/d$
> $f_c=n/2d\sqrt{\mu\epsilon}$
> Higher energy levels will require higher frequencies to attenuate.

So the $TM_0$ mode *is* a $TEM$ type wave. But what about for the TE waves?
> $f>f_c\to\gamma=jk$
> $f<f_c\to\gamma=\alpha$

