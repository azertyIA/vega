Imagine there is a current flowing in the $\hat z$ direction. Then there is a magnetic field in the azimuthal direction: $\vec H_\phi$. As such, the integral form of Ampere's Law:
> $\oint\vec H\cdot d\vec l=I$
> $\to2\pi rH_\phi=I$
> $\to H_\phi=I/2\pi r$

If there is a total current flowing through an area of wire, there are a few cases to measure the magnetic field:
> $r<a:H_\phi=I_{enc}/2\pi r=Ir/2\pi a^2\propto r$
> $r\geq a:H_\phi=I/2\pi r\propto 1/r$

A perfect conductor would not allow an E-field. The transformer is the most important thing we use today. We can swiftly turn such high voltage into a lower more manageable voltage using pure AC. We should be fairly familiar with the scenario we work with. For example, the antenna can both be seen as a cylinder as well as a sphere dependent on how far you are.

Imagine there is a loop containing a resistor right next to a current that generates a magnetic field. So, the magnetic field strength can be quantified by the distance from the current.
> $H_\phi=I/2\pi r$

The magnetic flux will create a flux through such a loop:
> $\Phi_B=\int d\vec s\cdot\vec B=\mu\int d\vec s\cdot\vec H$

So let's start subbing.
> $\Phi_B=\mu\int d(hr)\cdot H_\phi$
> $=\frac{\mu Ih}{2\pi}\int^c_b\frac{dr}{r}$
> $=\frac{\mu Ih}{2\pi}\ln\frac{c}{b}$

And now we can use Faraday's Law:
> $\nabla\times\vec E=-\partial_t\vec B\to\oint d\vec l\cdot\vec B=-\partial_t\Phi_B$
> $V_{ind}=-\partial_t\frac{\mu I}{2\pi}\ln\frac{c}{b}$, 

But when there is a constant current, there is no partial derivative. But in an AC situation, this changes fundamentally.

We spent a lot of time talking about steady states so we don't have to set up differential equations. Under steady state, we can use Euler's Rule to convert instantaneous states to phasor form. So, it's really easy.

Let's take Faraday's Law for example.
> $\nabla\times\vec E=-\mu\partial_t\vec H$
> $\vec E(\vec r,t)=\Re\vec E_s(\vec r)e^{j\omega t}$
> $\vec H(\vec r,t)=\Re\vec H_s(\vec r)e^{j\omega t}$
> $\nabla\times\Re\vec E_s(\vec r)e^{j\omega t}=-\mu\partial_t\Re\vec H_s(\vec r)e^{j\omega t}$
> $\nabla\times\Re\vec E_s(\vec r)e^{j\omega t}=-\mu\Re\vec H_s(\vec r)\partial_te^{j\omega t}$
> $\nabla\times\Re\vec E_s(\vec r)e^{j\omega t}=-\mu\Re j\omega\vec H_s(\vec r)e^{j\omega t}$
> $\Re\nabla\times\vec E_s(\vec r)=-\mu\Re j\omega\vec H_s(\vec r)$
> $\nabla\times\vec E_s(\vec r)=-j\omega\mu\vec H_s(\vec r)$

$\vec E_s$ can be written as its own wave:
> $\vec E_s(\vec r)=E_0e^{-jkz}$, $k$ is wave number = $\frac{2\pi}{\lambda}$

But you can put a vector quantity on this scalar for that particle to propagate in a direction. This uses the idea of plane waves, which are just very far away circular waves.
> $\vec k=\hat xk_x+\hat yk_y+\hat zk_z$
> $\vec r=\hat xx+\hat yy+\hat zz$
> $\vec k\cdot\vec r=k_xx+k_yy+k_zz$

Given light though, group velocity, phase velocity, and the speed of light are all the same.
> $c=\frac{1}{\sqrt{\mu_0\epsilon_0}}=\frac{\omega}{k}=\lambda f$

Or just use $\hbar\omega=hc/\lambda$. But let's get back to Faraday's law.
> $\nabla\times E_0e^{-j\vec k\cdot\vec r}=-j\omega\mu\vec H_s(\vec r)$
> $\hat k\cdot\vec E_s(\vec r)=\mu\omega\vec H_s(\vec r)=\sqrt{\frac{\mu}{\epsilon}}\vec H_s$
> $\hat k\cdot\vec E_s(\vec r)=\zeta\vec H_s$, $\zeta_0\approx120\pi$

$\zeta$, just like Z, represents impedance with unit Ohms analyzed under an AC circuit. Otherwise it would be called resistance if it was in the real DC domain.