The Type one superconductor has the following properties:
> $\vec B_{inside}=0$
> $\vec E_{inside}=0$
> $\vec J_{S}=0$
> $\rho_{S}=0$

For a cooper pair:
> $\psi(\vec x)=\sqrt{n_S}\exp i\theta(\vec x)$
> $|\psi(\vec x)|=n_S\exp (i\theta(\vec x)-i\theta(\vec x))=n_S$

We will now consider the washer topology:
> $\Pi=m\vec v=\vec p-q\vec A$ (em-vee momentum)
> $\vec p=-i\hbar\nabla$
> $q=-2e$
> $\vec J_S=nq\vec v=nq\Pi/m$

Applying the stuff:
> $(\vec p-q\vec A)\psi(\vec x)=(-i\hbar\nabla-q\vec A)\psi(\vec x)$
> $=(\hbar\nabla\theta-q\vec A)\psi(\vec x)$ (chain rule)

> $\oint(\hbar\nabla\theta-q\vec A)\psi(\vec x)$

> $-(\hbar/2e)\oint\nabla\theta\cdot d\vec l=\iint d\vec n\cdot\nabla\times\vec A$
> $=\iint d\vec n\cdot\vec B=\Phi_B$
> $=-2\hbar\pi/2e$
> $=-h/2e=\Phi_0$

In an S-I-S system, the cooper pair can tunnel through the insulator, keeping their entanglement.
> $i\hbar\partial_t\begin{pmatrix}\sqrt n_1e^{i\phi_1} \\ \sqrt n_2e^{i\phi_2}\end{pmatrix}=\begin{pmatrix}eV & K \\ K & -eV\end{pmatrix}\begin{pmatrix}\sqrt n_1e^{i\phi_1} \\ \sqrt n_2e^{i\phi_2}\end{pmatrix}$

> $i\hbar\partial_t\sqrt n_1e^{i\phi_1}=eV\sqrt n_1e^{i\phi_1} + K\sqrt n_2e^{i\phi_2}$
> $i\hbar(\partial_t\sqrt n_1e^{i\phi_1}+i\phi_1\sqrt n_1e^{i\phi_1})=eV\sqrt n_1e^{i\phi_1} + K\sqrt n_2e^{i\phi_2}$
> $i\hbar((1/2\sqrt n_1)\partial_tn_1e^{i\phi_1}+i\partial_t\phi_1\sqrt n_1e^{i\phi_1})=eV\sqrt n_1e^{i\phi_1} + K\sqrt n_2e^{i\phi_2}$
> $i\hbar(\partial_tn_1+2i\partial_t\phi_1n_1)=2eVn_1 + 2K\sqrt{n_2n_1}e^{i(\phi_2-\phi_1)}$
> $i\hbar\partial_tn_1-2\hbar\partial_t\phi_1n_1=2eVn_1 + 2K\sqrt{n_2n_1}e^{i(\phi_2-\phi_1)}$ (eq. 1)

> $i\hbar\partial_t\sqrt n_2e^{i\phi_2}=-eV\sqrt n_2e^{i\phi_2} + K\sqrt n_1e^{i\phi_1}$
> $i\hbar(\partial_t\sqrt n_2e^{i\phi_2}+i\sqrt n_2\partial_t\phi_2e^{i\phi_2})=-eV\sqrt n_2e^{i\phi_2} + K\sqrt n_1e^{i\phi_1}$
> $i\hbar((1/2\sqrt n_2)\partial_tn_2e^{i\phi_2}+i\sqrt n_2\partial_t\phi_2e^{i\phi_2})=-eV\sqrt n_2e^{i\phi_2} + K\sqrt n_1e^{i\phi_1}$
> $i\hbar((1/2\sqrt n_2)\partial_tn_2e^{i\phi_2}+i\sqrt n_2\partial_t\phi_2e^{i\phi_2})=-eV\sqrt n_2e^{i\phi_2} + K\sqrt n_1e^{i\phi_1}$
> $\hbar\partial_tn_2-2\hbar n_2\partial_t\phi_2=-2eVn_2 + 2K\sqrt{n_1n_2}e^{i(\phi_1-\phi_2)}$ (eq.2)

Taking the real and imaginary parts (there are four unknowns):
> $\partial_tn_1=-\partial_tn_2=2Kn_0\sin(\phi_2-\phi_1)/\hbar$
> $\partial_t(\phi_2-\phi_1)=2eV/\hbar\to\Delta\phi=2eVt/\hbar$

More interestingly we can look at the current:
> $I(t)=\partial_tq$
> $=2e\partial_tn_1$
> $=(2eK/\hbar)n_0\sin(\phi_2-\phi_1)$
> $=I_0\sin(2eVt/\hbar)$

For AC:
> $V(t)=(\hbar/2e)\partial_t\phi$
> $V_0e^{i\omega t}=(\hbar/2e)\partial_t\phi$
> $(V_0/\omega)e^{i\omega t}=(\hbar/2e)\phi+C$
> $V(t)/\omega=(\hbar/2e)\phi$
