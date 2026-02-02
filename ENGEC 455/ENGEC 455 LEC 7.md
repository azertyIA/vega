**Faraday**'s Law, yeah?
> $\nabla\times\vec E(\vec r,t)=-\partial_t\vec B(\vec r,t)$
> $\nabla\times\Re[\hat a_EE_0e^{-j\vec k\cdot\vec r}e^{j\omega t}]=-\partial_t\Re\hat a_BB_0e^{-j\vec k\cdot\vec r}e^{j\omega t}$
> $\Re[\nabla\times\hat a_EE_0e^{-j\vec k\cdot\vec r}e^{j\omega t}]=-\Re\hat a_BB_0e^{-j\vec k\cdot\vec r}\partial_te^{j\omega t}$
> $\Re[\nabla\times\hat a_EE_0e^{-j\vec k\cdot\vec r}e^{j\omega t}]=-\Re[\hat a_BB_0e^{-j\vec k\cdot\vec r}j\omega e^{j\omega t}]$
> $\Re[-e^{j\omega t}j\vec k\times\hat a_EE_0e^{-j\vec k\cdot\vec r}]=-\Re[\hat a_BB_0e^{-j\vec k\cdot\vec r}j\omega e^{j\omega t}]$
> $\Re[-j\vec k\times\hat a_EE_0e^{-j\vec k\cdot\vec r}e^{j\omega t}]=\Re[-\hat a_BB_0e^{-j\vec k\cdot\vec r}j\omega e^{j\omega t}]$
> $\Re[-j\vec k\times\vec E_s(\vec r)e^{j\omega t}]=\Re[-j\omega\vec B_s(\vec r)e^{j\omega t}]$
> $-j\vec k\times\vec E_s(\vec r)e^{j\omega t}=-j\omega\vec B_s(\vec r)e^{j\omega t}$
> $\vec k\times\vec E_s(\vec r,t)=\omega\mu\vec H_s(\vec r,t)$
> $\hat k\times\vec E_s(\vec r,t)=\frac\omega k\mu\vec H_s(\vec r,t)$
> $\hat k\times\vec E_s(\vec r,t)=v_{phase}\mu\vec H_s(\vec r,t)$
> $\hat k\times\vec E_s(\vec r,t)=\frac1{\sqrt{\mu\epsilon}}\mu\vec H_s(\vec r,t)$
> $\hat k\times\vec E_s(\vec r,t)=\sqrt{\frac\mu\epsilon}\vec H_s(\vec r,t)$
> $\hat k\times\vec E_s=\zeta\vec H_s$, $\zeta=120\pi=377$ Ohms.

Let's do a few examples:
> $E_s=\hat a_zE_0\exp[-j(5x-7y)]$
> $\vec k=5\hat a_x-7\hat a_y+0\hat a_z$
> $k=\sqrt{74}$
> $\omega=\sqrt{74}/c$

Imagine we have 2 mediums, each with their own $(\mu,\epsilon,\zeta)$. And there's an electric field in medium 1 before changing direction in medium 2. What is the new E-field? The old E-field hits the boundary at some angle, and can thusly be decoupled into two different components: tangent and normal to the boundary. This applies to the new field as well.
> $(E_{1tangent},E_{1normal})$
> $(E_{2tangent},E_{2normal})$

If the second medium is a conductor, then there can be no electric field in said conductor. Anyways, at the boundary, take a rectangular selection with width $w$ and height $h$. You now have a pretty nice contour. You can try selecting the boundary itself by having $w$ approach $0$. So, now apply Stoke's theorem:
> $\int d\vec s\cdot\nabla\times\vec E=\oint d\vec l\cdot\vec E=-\partial_t\int d\vec s\cdot\vec B\to0$, as we try to shrink the width.
> Eventually this should approach 0. So, no B field will be involved.
> $=\oint d\vec l\cdot\vec E=E_{1tangent}(l)+0+E_{2tangent}(-l)+0=0$
> $E_{1tangent}-E_{2tangent}=0$
> The tangential components will be the same under the boundary condition.

Ideally the this contour should include both regions for this to make the most sense. Now let's move to 3D:
> $\int dV\nabla\cdot\vec B=\int d\vec s\cdot\vec B=0$, $(\nabla\cdot\vec B=0)$
> $\vec B_1=\hat a_nB_{1n}+\hat a_tB_{1t}$
> $\vec B_2=-\hat a_nB_{2n}+\hat a_tB_{2t}$
> $0=\int d\vec s\cdot\vec B_1+\int d\vec s\cdot\vec B_2$
> $0=sB_1=-sB_2$
> $B_1=B_2$
> Magnetic field is continuous on the boundary.

What about the other two?
> $\nabla\times\vec H=\vec J_c+\partial_t\vec D$
> $\nabla\cdot\vec D=\rho$

Assuming an insulator for both mediums, $\vec J_c$ *has* to be $0$. Otherwise, the charge and current would have to be calculated at the boundary, making a surface rather than based on a volume.
