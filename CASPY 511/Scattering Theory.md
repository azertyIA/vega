How do we describe the probability of elastically scattering an incident monochromatic particle wave from a compact potential? In essence, all engineering problems are ones of this kind.

A compact scattering potential is defined like a sphere of potential that stops.
$$\exists d_{max}\in\mathbb R^+\text{ such that }\forall r'>d_{max},V(r')=0$$
As a result, because there is no scattering potential by the time of measurement, the particle is effectively a free particle with its energy completely preserved since its scatter. There is an incident wave $|k_0|=2\pi/\lambda$ and a radiation zone $|k_f|=2\pi/\lambda$.

In order to solve this problem, there exists a simple universal recipe called the **"First Born Approximation"** that is fully relativistic:
1. Fourier Transform the scattering potential.
2. Write down the answer.

The time dependent Schrodinger Equation should be:
$$[-\frac1{2m}\hbar^2\nabla^2+V(r)]\Psi(x,t)=[i\hbar\partial_t]\Psi(x,t)$$
But for monochromatic constant energy, the energy operator just gives us the one value:
$$i\hbar\partial_t\Psi(x,t)=\hbar\omega\Psi(x,t)\to\Psi(x,t)=\psi(x)e^{-i\omega t}$$
$$[-\frac1{2m}\hbar^2\nabla^2+V(r)]\psi(r)=\frac1{2m}\hbar^2k_0^2\psi(r)$$
$$\frac{\hbar^2}{2m}(\nabla^2+k_0^2)=V(r)\psi(r)$$
The incident plane wave takes the form of (it should also be normalized to $1/\sqrt{L^3}$)
$$\psi_0(r)\to e^{ik_0r}=e^{ikz}$$
For the outgoing wave, it should be dependent on the radius away from the source:
$$\psi_f(\vec r,t)\to\frac1re^{ik_f\cdot\vec r}f(\theta,\phi)$$
To find flux, we can just take the probability current density but with units:
$$\vec J_0=\frac\hbar{2m}2\Im(\psi_0^*\nabla\psi_0)=\frac{\hbar k_0}{2m}|\psi_0|^2\hat z$$
There is a 2D angle called $d\Omega$ that represents a section of the surface area of the sphere. 
> My mind blanked quite a bit.

If we take the equation we have for the potential we can rewrite RHS as the source:
$$(\nabla^2+k_0^2)\psi(r)=\frac{2m}{\hbar^2}V(r)\psi(r)=\tilde V(r)\psi(r)=source$$
$$(\nabla^2+k_0^2)\psi(r)=\tilde V(r)\psi(r)$$
We can pretend that this potential is made up of a bunch of tiny ass potentials or delta functions.
$$\boxed{(\nabla^2+k_0^2)G(r-r')=\delta(r-r')}$$
By solving G, we would integrate over all of r. The solution for the Green function is bound to the initial and boundary conditions.
$$\psi(r)=\psi_0(r)+\int d\vec r'G(\vec r-\vec r')\tilde V(\vec r')\psi(\vec r')$$
$$(\nabla^2+k_0^2)\psi_0(\vec r)=0$$
Let's try plugging it in:
$$(\nabla^2+k_0^2)(\psi_0(r)+\int d\vec r'G(\vec r-\vec r')\tilde V(\vec r')\psi(\vec r'))=0+\tilde V(r)\psi(r)$$
We can make a claim for the Green function:
$$G(\vec r-\vec r')=-\frac1{4\pi|\Delta r|}e^{ik_0|\Delta r|}$$
How did we do that? Try the FT:
$$(\nabla^2+k_0^2)G(\Delta r)=\delta(\Delta r)$$
$$G(\vec r)\to G_k(\vec k)=\int d\vec re^{-i\vec k\cdot\vec r}G(\vec r)$$
$$G(\vec k)\to G(\vec r)=\frac1{(2\pi)^3}\int d\vec ke^{+i\vec k\cdot\vec r}G_k(\vec k)$$
The Transformed Helmholtz equation gives us:
$$(-k^2+k_0^2)G_k(\vec k)=1$$
$$G_k(\vec k)=(-k^2+k_0^2)^{-1}$$
$$G(\vec r)=\frac1{(2\pi)^3}\int d\vec k\frac1{k_0^2-k^2}e^{+i\vec k\cdot\vec r}$$
But the final scatter ray $\vec k_f$ is defined to be $k_0\hat r$:
$$=\frac1{(2\pi)^3}\int dk k^2\int d\Theta\sin\Theta\int d\Phi\frac1{k_0^2-k^2}e^{+ikr\cos\theta}$$
$$=\frac1{(2\pi)^3}\int dk k^2\int d\Theta\sin\Theta\int d\Phi\frac1{k_0^2-k^2}e^{+ikr\cos\theta}$$
$$=\frac1{(2\pi)^3}\int dk k^2\int d\Theta\sin\Theta\int d\Phi\frac1{k_0^2-k^2}e^{+ik|\vec r-\vec r'|\cos\chi}$$
$$=\frac{+i}{(2\pi)^2r}\int dk \frac k{k_0^2-k^2}[e^{+ikr}-e^{-ikr}]$$
$$=\frac{+i}{(2\pi)^2r}(\int_0^\infty dk \frac k{k^2-k_0^2}e^{+ikr}+\int_{-\infty}^0 dK \frac K{K^2-k_0^2}e^{+iKr})$$
$$=\frac{+i}{(2\pi)^2r}\int_{-\infty}^\infty dk \frac k{k^2-k_0^2}e^{+ikr}$$
$$=\frac{+i}{(2\pi)^2r}\int_{-\infty}^\infty dk \frac k{(k+k_0)(k-k_0)}e^{+ikr}$$
$$=\frac{+i}{(2\pi)^2r}\int_{-\infty}^\infty d(k) \frac {(k)}{(k+k_0)(k-k_0)}e^{+ikr}$$
If we extend $k$ to the complex numbers with $k=k'+ik''$, then the exponential will have a blowing up part and a not so blowing up part depending on the sign of $k''$.
$$e^{ikr}=e^{ik'r}e^{-k''r}$$
So you should make a contour containing that 

The residue theorem states the following:
$$\oint dzf(z)=2\pi i\Sigma\lim_{z\to z_0}[(z-z_0)f(z)]$$

We end up getting four different universes, but the positive poles should decay while the negative poles should explode, as that would indicate the arrow of time. The others are one with no scattering, one with reversed time and one with standing waves. To solve this problem:
$$f(k)=ke^{+ikr}/(k+k_0)(k-k_0)$$
$$\oint dkf(k)=2\pi i\lim[(k-k_0)ke^{+ikr}/(k+k_0)(k-k_0)]$$
$$=2\pi i\lim[ke^{+ikr}/(k-k_0)]$$
$$G(\vec r-\vec r')=-\frac1{4\pi|\Delta r|}e^{ik_0|\Delta r|}$$
Creating a wavefunction demands the following.
$$\psi(r)=\psi_0(r)+\int d\vec r'G(\vec r-\vec r')\tilde V(\vec r')\psi(\vec r')$$
Now just approximate through the potential answers just as the Dyson series follows:
$$\psi(r)=e^{+ikz}$$
$$\psi(r)=e^{+ikz}+\int d\vec r'G(\vec r-\vec r')\tilde V(\vec r')e^{+ikz'}$$
$$=e^{+ikz}-\frac1{4\pi}\int d\vec r'\frac{e^{ik_0|\Delta r|}}{|\Delta r|}\tilde V(\vec r')e^{+ikz'}$$
But usually in the radiation zone, $r'$ is usually going to be much, much smaller than $r$, so the pre-factor can just be $r$:
$$=e^{+ikz}-\frac1{4\pi r}\int d\vec r'{e^{ik_0|\Delta r|}}\tilde V(\vec r')e^{+ikz'}$$
$$=e^{+ikz}-\frac{2m}{4\pi\hbar^2 r}V_q(\vec q)e^{+ikr}$$
Where $q$ is defined as $2k_0\sin\frac\theta2$

## First Born Approximation
$$V(\vec r)=\frac{V_0b^3}2[\delta(\vec r+\frac d2\hat x)+\delta(\vec r-\frac d2\hat x)]$$
$$V_q(\vec q)=\int d^3x'V(\vec r)e^{-i\vec q\cdot\vec r}$$
$$=\frac{V_0b^3}2\int d^3x'[\delta(\vec r+\frac d2\hat x)+\delta(\vec r-\frac d2\hat x)]e^{-i\vec q\cdot\vec r}$$
$$=\frac{V_0b^3}2[e^{-i\vec q\cdot\frac d2\hat x}+e^{-i\vec q\cdot-\frac d2\hat x}]$$
$$={V_0b^3}\cos(\vec q\cdot\frac d2\hat x)$$
$$\partial_\Omega r=\frac{m^2(V_0b^3)^2}{4\pi^2\hbar^4}\cos^2(\frac{k_0d}2\sin\theta)$$
This value has its maximum at $k_0d\sin\theta=2\pi n$, which gets you the following property:
$$d\sin\theta=n\lambda$$
