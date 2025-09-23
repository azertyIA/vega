#PY511
## 2.1. Pauli Spins Again?

$U_3(\theta,\phi,\lambda)=\begin{pmatrix}\cos\frac{\theta}{2}&-e^{i\lambda}\sin\frac{\theta}{2}\\e^{i\phi}\sin\frac{\theta}{2}&e^{i\lambda+i\phi}\cos\frac{\theta}{2}\end{pmatrix}$

a.i. $\sigma_x$
> $\cos\frac{\theta}{2}=0$
> $-e^{i\lambda}\sin\frac{\theta}{2}=1$
> $e^{i\phi}\sin\frac{\theta}{2}=1$
> $\Im(e^{i\lambda})=\Im(e^{i\phi})=0=\sin\lambda=\sin\phi$

> $\theta=(2n+1)\pi$ 
> $\lambda=(n+1)\pi$
> $\phi=n\pi$

a.ii. $\sigma_y$
> $\cos\frac{\theta}{2}=0$
> $-e^{i\lambda}\sin\frac{\theta}{2}=-i$
> $e^{i\phi}\sin\frac{\theta}{2}=i$
> $\Re(e^{i\lambda})=\Re(e^{i\phi})=0=\cos\lambda=\cos\phi$

> $\theta=(2n+1)\pi$ 
> $\lambda=\frac{2n+1}{2}\pi$
> $\phi=\frac{2n+1}{2}\pi$

a.iii. $\sigma_z$
> $\sin\frac{\theta}{2}=0$
> $\cos\frac{\theta}{2}=1$
> $e^{i\lambda+i\phi}=-1$
> $\Im(e^{i\lambda+i\phi})=0=\sin(\lambda+\phi)$

> $\theta=2n\pi$ 
> $\lambda+\phi=(2m+1)\pi$

a.iv. $U^\dagger=U^{-1}$
> $U^\dagger U=I$
> $=\begin{pmatrix}\cos\frac{\theta}{2}&e^{-i\phi}\sin\frac{\theta}{2}\\-e^{-i\lambda}\sin\frac{\theta}{2}&e^{-i\lambda-i\phi}\cos\frac{\theta}{2}\end{pmatrix}\begin{pmatrix}\cos\frac{\theta}{2}&-e^{i\lambda}\sin\frac{\theta}{2}\\e^{i\phi}\sin\frac{\theta}{2}&e^{i\lambda+i\phi}\cos\frac{\theta}{2}\end{pmatrix}$
> $=\begin{pmatrix}\cos^2\frac{\theta}{2}+sin^2\frac{\theta}{2}&(e^{i\lambda}-e^{i\lambda})(\cos\cdot\sin)\frac{\theta}{2}\\(e^{-i\lambda}-e^{-i\lambda})(\sin\cdot\cos)\frac{\theta}{2}&\sin^2\frac{\theta}{2}+\cos^2\frac{\theta}{2}\end{pmatrix}$
> $=I$
> It will be unitary all the time.

a.b. $H=g_0I+\vec{g}\cdot\vec{\sigma}=\hbar\Omega U$
> $=\begin{pmatrix}g_0+g_3&g_1-ig_2\\g_1+ig_2&g_0-g_3\end{pmatrix}$
> $\to\hbar\Omega\cos\frac{\theta}{2}=g_0+g_3$
> $\to-\hbar\Omega\cos\lambda\sin\frac{\theta}{2}=\hbar\Omega\cos\phi\sin\frac{\theta}{2}=g_1$
> $\to\hbar\Omega\sin\lambda\sin\frac{\theta}{2}=\hbar\Omega\sin\phi\sin\frac{\theta}{2}=g_2$
> $\to\hbar\Omega\sin(\lambda+\phi)\cos\frac{\theta}{2}=0$
> $\to\hbar\Omega\cos(\lambda+\phi)\cos\frac{\theta}{2}=g_0-g_3$

If $\theta\neq2m\pi$ ($\sin\frac{\theta}{2}\neq0$), then:
> $-\cos\lambda=\cos\phi$
> $\sin\lambda=\sin\phi$
> $\to\lambda+\phi=(2n+1)\pi$

If $\theta=2m\pi$ ($\cos\frac{\theta}{2}\neq0$), then:
> $\sin(\lambda+\phi)=0$
> $\to\lambda+\phi=n\pi$
### If $\theta\neq2m\pi:$
> $g_0=\frac{1}{2}(g_0+g_3+g_0-g_3)$
> $=\frac{1}{2}\hbar\Omega(1+\cos(\lambda+\phi))\cos\frac{\theta}{2}$
> $=\frac{1}{2}\hbar\Omega(1+\cos((2n+1)\pi)\cos\frac{\theta}{2}$
> $=\frac{1}{2}\hbar\Omega(1-1)\cos\frac{\theta}{2}$
> $=0$
> $g_1=\hbar\Omega\sin\frac{\theta}{2}\cos\phi$
> $g_2=\hbar\Omega\sin\frac{\theta}{2}\sin\phi$
> $g_3=\frac{1}{2}(g_0+g_3-g_0+g_3)$
> $=\frac{1}{2}\hbar\Omega(1-\cos(\lambda+\phi))\cos\frac{\theta}{2}$
> $=\frac{1}{2}\hbar\Omega(1-\cos((2n+1)\pi)\cos\frac{\theta}{2}$
> $=\frac{1}{2}\hbar\Omega(1+1)\cos\frac{\theta}{2}$
> $=\hbar\Omega\cos\frac{\theta}{2}$

Checking for Hermitian:
> $=\begin{pmatrix}\hbar\Omega\cos\frac{\theta}{2}&\hbar\Omega\sin\frac{\theta}{2}(\cos\phi-i\sin\phi)\\\hbar\Omega\sin\frac{\theta}{2}(\cos\phi+i\sin\phi)&-\hbar\Omega\cos\frac{\theta}{2}\end{pmatrix}$
> $\to\begin{pmatrix}\hbar\Omega\cos\frac{\theta}{2}&\hbar\Omega\sin\frac{\theta}{2}(\cos\phi-i\sin\phi)\\\hbar\Omega\sin\frac{\theta}{2}(\cos\phi+i\sin\phi)&-\hbar\Omega\cos\frac{\theta}{2}\end{pmatrix}^\dagger$
> $=\begin{pmatrix}\hbar\Omega\cos\frac{\theta}{2}&\hbar\Omega\sin\frac{\theta}{2}(\cos\phi-i\sin\phi)\\\hbar\Omega\sin\frac{\theta}{2}(\cos\phi+i\sin\phi)&-\hbar\Omega\cos\frac{\theta}{2}\end{pmatrix}$
> For all matrices of this case, the matrix is Hermitian.
### If $\theta=2m\pi:$
> $g_0=\frac{1}{2}(g_0+g_3+g_0-g_3)$
> $=\frac{1}{2}\hbar\Omega(1+\cos(\lambda+\phi))\cos\frac{\theta}{2}$
> $=\frac{1}{2}\hbar\Omega(1+\cos n\pi)\cos m\pi\in\{\hbar\Omega,-\hbar\Omega,0\}$
> $g_1=g_2=0$
> $g_3=\frac{1}{2}(g_0+g_3-g_0+g_3)$
> $=\frac{1}{2}\hbar\Omega(1-\cos(\lambda+\phi))\cos m\pi$
> $=\frac{1}{2}\hbar\Omega(1-\cos n\pi)\cos m\pi\in\{\hbar\Omega,-\hbar\Omega,0\}$
> Because of $\cos n\pi$, only one of $g_0$ or $g_1$ can be $0$ while the other is $\pm\hbar\Omega$.

Checking for Hermitian:
> It's a diagonal matrix without imaginary numbers; the matrix is Hermitian.

Therefore, as long as the U gate can be represented in the form of $g_0I+\vec{g}\cdot\vec{\sigma}$, the resulting matrix will be Hermitian for all values of $\theta$ and resulting valid values of $\phi$ and $\lambda$.
> If $\theta\neq2m\pi:\lambda+\phi=(2n+1)\pi$
> If $\theta=2m\pi:\lambda+\phi=n\pi$

c.i. $\{\sigma_i,\sigma_j\}$
> $=\sigma_i\sigma_j+\sigma_j\sigma_i$
> $i=j:2\sigma_i^2=2I$
> $i\neq j:\sigma_i\sigma_j-\sigma_i\sigma_j=0$
> $=2\delta_{ij}I$

c.i. $\{\vec{a}\cdot\vec{\sigma},\vec{b}\cdot\vec{\sigma}\}$
> $=(\vec{a}\cdot\vec{\sigma})(\vec{b}\cdot\vec{\sigma})+(\vec{b}\cdot\vec{\sigma})(\vec{a}\cdot\vec{\sigma})$
> $=\Sigma \{a_i\sigma_i,b_j\sigma_j\}$
> $=\Sigma a_ib_j\{\sigma_i,\sigma_j\}$
> $=\Sigma 2a_ib_j\delta_{ij}I$
> $=2\Sigma ab=2(\vec{a}\cdot\vec{b})I$
## 2.2. Photoelectric Effect

Start with Planck's constants:
> $G=\hbar=c=k_B=1$
> $\hbar=\frac{h}{2\pi}=\frac{1}{2\pi}$

What is a second?
> $\text{1 s}=\text{1 s}\times\frac{2\pi\hbar}{h}\times\frac{h}{6.626\times10^{-34}\text{J-s}}\times\frac{1.602\times10^{-19}\text{J}}{\text{1 eV}}=1.608\times10^{-14}\hbar\text{/eV}=1.608\times10^{15}\text{eV}^{-1}$

And a meter?
> $\text{1 m}=\text{1 m}\times\frac{\text{c}}{\text{299792458 m/s}}\times\frac{1.608\times10^{15}\text{eV}^{-1}}{\text{1 s}}=5.363\times10^6\text{eV}^{-1}$

> $W=4.2$ eV, $\lambda=200$ nm, $P=100$ mW

Photoelectric effect states that the voltage can be given by the following relation:
> $eV=T=E(\nu)-W=h\nu-h\nu_0$, where $\nu_0$ is the minimum frequency needed to see current.
> $eV=2\pi\hbar c/\lambda-W$
