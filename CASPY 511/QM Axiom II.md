#PY511 
The second of five [[QM Axioms]].
## Quantum Mechanics

When moving to quantum mechanics from [[Hamiltonian Mechanics]], the Poisson Brackets are replaced with commutators to satisfy Heisenberg's Uncertainty Principle:
$$\{q,p\}=1\to[\hat q, \hat p]=i\hbar$$
Normalizing this gets us a general method to convert Poisson Brackets to quantum commutators. This in turn, will grant us with the equation of motion.
$$\{A,B\}\to\frac 1{i\hbar}[\hat A, \hat B]$$
$$\partial_tA=\{A,H\}\to i\hbar\partial_t\hat A=[\hat A, \hat H]$$
$$i\hbar\partial_t\hat A(t)\ket\psi=[\hat A(t),\hat H]\ket\psi$$
Assume the existence of a time-evolution operator $U(t_0,t)$ such that it acts on a ket to evolve it further in time:
$$U(t_0,t)\ket{\psi,t_0}=\ket{\psi,t}$$
$$\bra{\psi,t_0}U^{\dagger}(t_0,t)=\bra{\psi,t}$$
We can now shift our operator to a time-independent Schrodinger picture:
$$\bra{\psi,t_0}\hat A(t)\ket{\psi,t_0}=\braket{\psi,t|\hat A_S|\psi,t}$$
$$\boxed{\hat A(t)=\hat U^\dagger(t_0,t)\hat A_S\hat U(t_0,t)}$$
$$\partial_t\hat A(t)=\partial_t\hat U^\dagger\hat A_S\hat U+\hat U^\dagger\hat A_S\partial_t\hat U=\frac 1{i\hbar}[\hat U^\dagger \hat A_S\hat U,\hat H]$$
However, the Hamiltonian shouldn't change over time. If it did then, it would also have time evolution operators and it would be bubbled up inside anyways.
$$=\partial_t\hat U^\dagger\hat A_S\hat U+\hat U^\dagger\hat A_S\partial_t\hat U=\frac 1{i\hbar}(\hat U^\dagger \hat A_S\hat H\hat U-\hat U^\dagger\hat H \hat A_S\hat U)$$
$$=\partial_t\hat U^\dagger\hat A_S\hat U+\hat U^\dagger\hat A_S\partial_t\hat U=\hat U^\dagger \hat A_S(\frac 1{i\hbar}\hat H)\hat U-(\frac 1{i\hbar}\hat H)\hat U^\dagger\hat A_S\hat U$$
Luckily associativity will always work:
$$=(\partial_t\hat U)^\dagger\hat A_S\hat U+\hat U^\dagger\hat A_S(\partial_t\hat U)=\hat U^\dagger \hat A_S(\frac 1{i\hbar}\hat H\hat U)+(\frac 1{i\hbar}\hat H\hat U)^\dagger\hat A_S\hat U$$
$$=(\partial_t\hat U)^\dagger\hat A_S\hat U+\hat U^\dagger\hat A_S(\partial_t\hat U)=\hat U^\dagger \hat A_S(\frac 1{i\hbar}\hat H\hat U)+(\frac 1{i\hbar}\hat H\hat U)^\dagger\hat A_S\hat U$$
So we're led to believe that the Hamiltonian has something to do with the derivative of the time evolution operator. But this is very powerful.
$$i\hbar\partial_t\hat U=\hat H\hat U$$
$$i\hbar\partial_t\hat U\ket{\psi,t_0}=\hat H\hat U\ket{\psi,t_0}$$
$$\boxed{i\hbar\partial_t\ket{\psi,t}=\hat H\ket{\psi,t}}$$
Axiom II is set, and the time evolution operator given a time-independent Hamiltonian has the following form:
$$\hat U(t)=\exp(t\partial_t)=\exp(-i\hat Ht/\hbar)$$

Here it should be noted that this behavior is in operator "Banach" space. A space without norms defined by an inner product. The two operators are identical.

The following should also be noted. Nothing happens in an instant of time, so this evolutionary operator does "nothing" when the time doesn't change.
> $\hat U(t_0,t_0)=\hat I$

All observables are Hermitian. If $U$ is Hermitian, then it is observable.
> $\partial_t\hat U(t,t_0)^\dagger=\frac{i}{\hbar}\hat U^\dagger(t,t_0)\hat H(t)$

It's probably not observable.

Axiom 4 says that $\braket{\psi(t)\mid\psi(t)}=1$, so what happens if we try to substitute the bras?
> $\bra{\psi,t_0}U^\dagger(t,t_0)U(t,t_0)\ket{\psi,t_0}$

Doing this the other way would lead you believe that $U^\dagger=U^{-1}$ or a *unitary* matrix.

What do Unitary operators do? This one just brings it forward in time. The unitary operator should bring you backwards in time. Or at least the other way.
> $U^{-1}(t,t_0)=U^\dagger(t,t_0)=U(t_0,t)$

Let's try solving anything, but let's set some cases:
1. $\hat H$ is time-independent. (trivial)
2. $\hat H$ is time-dependent but "commutes with itself" for all $t$. (straightforward)
3. $\hat H$ is generally dependent.
#### Guess for time-independence
The most obvious guess is an exponential one.
> $\hat U(t,t_0)=\exp(-\frac{i}{\hbar}(t-t_0)\hat H)$
> $=\Sigma\frac{1}{n!}(\frac{-i}{\hbar})^n(t-t_0)^n\hat H^n$
> $=\frac{-i}{\hbar}\hat H\Sigma_1\frac{1}{n!}(t-t_0)^n\hat H^n$

#### The Two Level System (TLS)
This system can be applied when there's two states something can have. But mostly energy.
> $\ket{\Psi,t}=\hat U(t,t_0)\ket{\Psi,t_0}$
> $\ket{\Psi,t_0}=c_0'\ket{0}+c_1'\ket{1}$

Now let's apply some stuff:
> $\ket{\Psi,t}=\hat U(t,t_0)\ket{\Psi,t_0}$
> $\ket{\Psi,t_0}=c_0'\ket{0}c_1'\ket{1}$
> $\ket{\Psi,t}=c_0'e^{-\frac{i}{\hbar}(t-t_0)E_0}\ket{0}+c_1'\ket{1}e^{-\frac{i}{\hbar}(t-t_0)E_1}$

If this was a classical wave amplitude then we expect to detect a signal at two frequencies. We should be obtaining it using the FFT. (Fast Fourier Transform). The first energy would be corresponding to $\hbar\omega_0/2$ and the second $3\hbar\omega_0/2$. 

But we never see two frequencies at the same time. In QM, we only see a frequency in the middle: $E_1-E_0/\hbar$. This is called precession.
> $\ket{\Psi,t}=c_0'e^{-\frac{i}{\hbar}(t-t_0)E_0}\ket{0}+c_1'\ket{1}e^{-\frac{i}{\hbar}(t-t_0)E_1}$

We can multiply this by $e^{+\frac{i}{\hbar}tE_0}$ and the two will be equal because multiplying the wavefunction by any complex number, it will basically be the same, as per Axiom 1:
> $\ket{\Psi,t}=c_0'\ket{0}+c_1'\ket{1}e^{-\frac{i}{\hbar}(t-t_0)(E_1-E_0)}$
> $\ket{\Psi,t}=c_0'\ket{0}+c_1'\ket{1}e^{-i\omega_0t}$
> You only see the frequency differences. ($\omega_0$)

Even for a time-independent Hamiltonian, the state ket will always be time dependent. However, there is no observable you can perform that shows this behavior.
> $\ket{\Psi,t}=e^{-\frac{i}{\hbar}\hat H_nt}\ket{n}$
> $\ket{\Psi,t}=e^{-\frac{i}{\hbar}E_nt}\ket{n}$
> Where $\ket{n}$ is a state with $E_n$ energy.
