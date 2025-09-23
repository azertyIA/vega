Here's a weird factoid:
> All Two-Level Systems are the same (isomorphic).

Let's start with angular momentum. Spin can't be a cross product in vectors, even though it's a form of angular momentum. If normal angular momentum can be represented in terms of a multiple of something then so should spin:
> $L=n\hbar$
> $S=?\hbar$

Angular momentum can be quantized:
> $\mu_e=-g_e\mu_e\cdot\frac1\hbar\vec S=\gamma_e\vec S$
> $\hat H=-\mu_e\cdot\vec B$
> $\mu_B=|\mu_e|=\frac{e\hbar}{2m_e}$
> $\gamma_e=g_e\frac{e}{2m_e}$
> $\nu_e=\frac{\omega_e}{2\pi}=28\text{ GHz}$

Meanwhile the mass of a proton (charge + spin) creates a frequency of $\text{42.577 MHz}$. A neutron (just spin) has a precession frequency of $\text{-29.16 MHz}$.

So let's start with the Hamiltonian:
> $\hat H=-\frac1 2\hbar\omega_L\sigma_\delta$

The spin-$\frac 1 2$ system has up and down:
> $\ket{\Psi}=\begin{pmatrix}\alpha \\ \beta\end{pmatrix}$
> $\hat H=\begin{pmatrix}H_{00}&H_{01}\\ H_{10}&H_{11}\end{pmatrix}$, $\hat H=\hat H^\dagger$

There is only one Hamiltonian, and it looks like a 2D matrix.
> $\hat H=\Sigma H_{nm}\ket n\bra m$
> Each ket-bra outer product is a basis for the Hamiltonian.

But it really sucks at being Hermitian. So let's use Pauli Matrices instead:
> $\hat H=\epsilon_0I+\sigma\cdot\vec\epsilon$

In a magnetic field:
> $\vec B=B\hat n\to\hat H=-\hbar B\gamma_P\sigma\cdot\hat n$

So now let's write in abstract space:
> $\vec S=\frac\hbar2\vec\sigma$

We can pretend n is written as a polar form in rectangular space, so substituting we get:
> $\vec\sigma\cdot\hat n=\begin{pmatrix}\cos\theta&\sin\theta e^{-i\phi}\\sin\theta e^{+i\phi}&-\cos\theta\end{pmatrix}$

The eigenvalues to this are $\lambda=\pm1$. The eigenvectors requires a little more thinking. We know that the phase doesn't matter and that the two components have a hypotenuse of one. So, knowing this, we can set the top part to a cosine of $\gamma$ and the bottom to the sine of $\gamma$ with some complex phase $\eta$.
> $\ket{\Psi}_{+1}=\cos\frac\theta2\ket{0}+e^{+i\phi}\sin\frac\theta2\ket{1}$
> $\ket{\Psi}_{-1}=\cos\frac\theta2\ket{0}+e^{-i\phi}\sin\frac\theta2\ket{1}$

So we can plot nearly anything on a Block Sphere. And It looks like spherical coordinates. They physically aren't perpendicular but their states are still orthogonal. Just some spinor shit.