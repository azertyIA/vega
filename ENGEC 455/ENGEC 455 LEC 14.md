I love Maxwell!!!!
> $\nabla\cdot\vec D=\rho$
> $\nabla\cdot\vec B=0$
> $\nabla\times\vec E=-\partial_t\vec B$
> $\nabla\times\vec H=\vec J_C+\partial_t\vec D$

In phasor form:
> $\nabla\cdot\mathbb{D}=\mathbb\rho$
> $\nabla\cdot\mathbb B=0$
> $\nabla\times\mathbb E=-j\omega\mathbb B$
> $\nabla\times\mathbb H=\mathbb J_C+j\omega\mathbb D$

For source free region:
> $\nabla\cdot\mathbb{D}=0$
> $\nabla\cdot\mathbb B=0$
> $\nabla\times\mathbb E=-j\omega\mathbb B$
> $\nabla\times\mathbb H=j\omega\mathbb D$

And solving:
> $\omega^2\epsilon\mu\mathbb E=\nabla\times(-j\omega\mu\mathbb H)=\nabla\times(\nabla\times\mathbb E)$
> $=\nabla\cdot(\nabla\cdot\mathbb E)-\nabla^2\mathbb E$
> $=\nabla\cdot(0)-\nabla^2\mathbb E$
> $\to0=(\nabla^2+\omega^2\mu\epsilon)\mathbb E$
> $=(\nabla^2+\omega^2/c^2)\mathbb E$
> $=(\nabla^2+k^2)\mathbb E$

There are three families of waveguide waves:
> TEM: $E\perp H\perp k=k\hat z,E_z=H_z=0$
> TE: $E\perp H,E \perp k,H_z\neq0=E_z$
> TM: $H\perp E,H \perp k,E_z\neq0=H_z$

For TM waves:
> $E_z=E_{xy}e^{-\gamma z}$
> $\nabla^2E_z=(\nabla_{xy}^2+\partial_z^2)(E_{xy}e^{-\gamma z})$
> $=\nabla_{xy}^2E_z+\gamma^2E_z$
> $=\partial_y^2E_z+\gamma^2E_z$

For the parallel plate waveguide extended to infinity, we don't care about the x axis because at large it just disappeared.
> $=(\partial_y^2+\gamma^2+k^2)\mathbb E$
> $=(\partial_y^2+h^2)\mathbb E$

The Faraday cage has NO electric field penetration. So, you get an electron in a box kind of equation. 
> $E_z=A\sin(\pi ny/d)$
> $A$ comes from power.

Now, if $H_z=0$, then that means $\partial_xE_y-\partial_yE_x=0$
> $\partial_xE_y=\partial_yE_x=0$
