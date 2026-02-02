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

Let's consider a spin-1/2 proton in a uniform B field. Magnetic waves could either be linear, circular, or ellipse in polarization. 
> $\vec B(t)=B_0\hat z+B_1\hat e_x\cos\omega t$
> $\vec B(t)=B_0\hat z+B_1(\hat e_x\cos\omega t+\hat e_y\sin\omega t)$
> $\vec B(t)=B_0\hat z+B_1(\hat e_x\cos\omega t-\hat e_y\sin\omega t)$

So the Hamiltonian:
> $\hat H=-\frac12\hbar\omega_L\sigma_z-\frac12\hbar\Omega_1(\sigma_x\cos\omega t-\sigma_y\sin\omega t)$ (circular clockwise case)

No exact solution is known for the linear case. But let's put everything in a matrix:
> $\hat H=\begin{pmatrix}-\frac12\hbar\omega_L&\frac12\hbar\Omega_1e^{+i\omega t}\\\frac12\hbar\Omega_1e^{-i\omega t}&+\frac12\hbar\omega_L\end{pmatrix}=\hat H_0+\hat V(t)$
> $\hat H_0=\begin{pmatrix}-\frac12\hbar\omega_L&0\\0&+\frac12\hbar\omega_L\end{pmatrix}$
> $\hat V=\begin{pmatrix}0&\frac12\hbar\Omega_1e^{+i\omega t}\\\frac12\hbar\Omega_1e^{-i\omega t}&0\end{pmatrix}$

In PY452, you would use the Schrodinger picture:
> $i\hbar\partial_t\ket{\Psi_s(t)}=\hat H_S\ket{\Psi_S(t)}$
> $\ket{\Psi_S(t)}=\alpha_0(t)\ket0+\alpha_1(t)\ket1$

Then just solve the differential equations. However in the Dirac Interaction Picture:
> $\ket{\Psi_I,t}=e^{-\frac1{i\hbar}\hat H_0t}\ket{\Psi_S}$
> $i\hbar\partial_t\ket{\Psi_I,t}=e^{-\frac1{i\hbar}\hat H_0t}\hat V(t)e^{+\frac1{i\hbar}\hat H_0t}\ket{\Psi_S}$

Now we can work in a diagonal matrix. Recall that the Interaction Picture multiplies the the state by the opposite time evolutionary term, thereby putting the "operators to rest."  Dirac's picture is the crowd, Heisenberg's is the ball and Schrodinger's is the world.

Rabi had an amazing idea. What if we created a rotating frame, where we can just jump onto the $\vec B_1$ frame.
> $\ket{\Psi_R,t}=e^{-\frac{i\omega t\sigma_z}2}\ket{\Psi_S,t}$
> $i\hbar\partial_t\ket{\Psi_R,t}=\hat H\ket{\Psi_R,t}$
> $i\hbar\partial_t(e^{-\frac{i\omega t\sigma_z}2}\ket{\Psi_S,t})$
> $i\hbar((-\frac{i\omega\sigma_z}2)e^{-\frac{i\omega t\sigma_z}2}\ket{\Psi_S,t}+e^{-\frac{i\omega t\sigma_z}2}\partial_t\ket{\Psi_S,t})$
> $(i\hbar(-\frac{i\omega\sigma_z}2)e^{-\frac{i\omega t\sigma_z}2}\ket{\Psi_S,t}+e^{-\frac{i\omega t\sigma_z}2}(\hat H_0+\hat V_S(t))\ket{\Psi_S,t})$
> $(-i\hbar\frac{i\omega\sigma_z}2e^{-\frac{i\omega t\sigma_z}2}\ket{\Psi_S,t}+e^{-\frac{i\omega t\sigma_z}2}(\hat H_0+\hat V_S(t))\ket{\Psi_S,t}$
> $(\frac12\hbar\omega\sigma_ze^{-\frac{i\omega t\sigma_z}2}+e^{-\frac{i\omega t\sigma_z}2}(\hat H_0+\hat V_S(t))\ket{\Psi_S,t}$
> $(\frac12\hbar\omega\sigma_z+e^{-\frac{i\omega t\sigma_z}2}(\hat H_0+\hat V_S(t))e^{+\frac{i\omega t\sigma_z}2})\ket{\Psi_R,t}$ ($H_0$ commutes with the exponential)
> $(\frac12\hbar(\omega-\omega_L)\sigma_z+e^{-\frac{i\omega t\sigma_z}2}\hat V_S(t)e^{+\frac{i\omega t\sigma_z}2})\ket{\Psi_R,t}$
> $(\frac12\hbar(\omega-\omega_L)\sigma_z+e^{-\frac{i\omega t\sigma_z}2}\hat V_S(t)e^{+\frac{i\omega t\sigma_z}2})\ket{\Psi_R,t}$

The second term is literally:
> $\begin{pmatrix}0&\gamma\\\gamma&0\end{pmatrix}$

So now we just solve for the Hamiltonian which can give us the probability. Which I won't write out.
> $P_{0\to1}(t)=(1+\frac{\hbar(\omega-\omega_L)}{2\gamma}^2)^{-1}\sin^2(\frac\gamma\hbar\sqrt{1+\frac{\hbar(\omega-\omega_L)}{2\gamma}^2}t)$ (generalized Rabi frequency)

The frequency domain when you change the detuning gives you a Lorentzian.

Now you can pulse this shit with some time and you get any gate at some angle. This frame really just cancels out the natural precession.