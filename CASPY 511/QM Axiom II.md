#PY511 
## Evolution
Given:
> $\ket{\Psi(t_0)}=\ket{\psi_0}$

One important things about axiom 2 is that it works on a time derivative and a Hamiltonian:
> $i\hbar\partial_t\ket{\Psi(t)}=\hat H(t)\ket{\Psi(t)}$
> $\partial_t\ket{\Psi(t)}=-\frac{i}{\hbar}\hat H(t)\ket{\Psi(t)}$

Because $\psi_0$ is in the same space as $\psi(t)$ there should be some mapping from one vector to the next. Let's say this mapping depends on both $t$ and $t_0$:
> $\ket{\Psi(t)}=\hat U(t, t_0)\ket{\Psi(t_0)}$ (time evolution operator)

What is the equation satisfied by $\hat U(t,t_0)$? How can we get here from the original Hamiltonian evolution? 

As an aside, for the sake of it whatever's inside the "ket" is just a label, as long as it's unique:
> $\ket{\Psi, t}=\ket{\Psi(t)}$
> $\ket{n}=\ket{(n+\frac{1}{2})\hbar\omega_0}$

You *should not* manipulate the stuff inside the "ket." It is just a label.
> $\ket{2n}\neq2\ket{n}=\ket{n}$

Back to it. Just take the old equation and plug in a $\hat U$:
> $i\hbar\partial_t\hat U(t,t_0)\ket{\Psi(t)}=\hat H(t)\hat U(t,t_0)\ket{\Psi(t)}$
> $[i\hbar\partial_t\hat U(t,t_0)]\ket{\Psi(t)}=[\hat H(t)\hat U(t,t_0)]\ket{\Psi(t)}$
> $i\hbar\partial_t\hat U(t,t_0)=\hat H(t)\hat U(t,t_0)$
> $\partial_t\hat U(t,t_0)=-\frac{i}{\hbar}\hat H(t)\hat U(t,t_0)$

Or written differently:
> $\frac{\partial\hat U(t,t_0)}{\partial t}=-\frac{i}{\hbar}\hat H\hat U(t,t_0)$

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
> 	$\ket{\Psi,t}=e^{-\frac{i}{\hbar}E_nt}\ket{n}$
> Where $\ket{n}$ is a state with $E_n$ energy.
