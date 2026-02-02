Acting on [[QM Axiom II]], The Schrodinger picture is the equation we've been learning:
> $\ket{\Psi,t}=\hat U(t,t_0)\ket{\Psi,t_0}$

Consider a Hermitian operator $\hat A^{(s)}$:
> $\braket{A}=\bra{\Psi,t}\hat A^{(s)}\ket{\Psi,t}$
> $=\bra{\Psi,t_0}\hat U^\dagger\hat A^{(s)}\hat U\ket{\Psi,t_0}$

Now we have a new operator in between the bras and kets, the Heisenberg picture:
> $\hat A^{(H)}=\hat U^\dagger\hat A^{(s)}\hat U$

Now we have the following equality between the two pictures:
> $\braket{A}=\bra{\Psi,t}\hat A^{(s)}\ket{\Psi,t}=\bra{\Psi,t_0}\hat A^{(H)}\ket{\Psi,t_0}$

The Schrodinger picture has a state that is time dependent. Operators like position, momentum, and spin are all time-independent. Meanwhile, the state is independent ($t_0$) while the the operators all transform and change to time.
> $\hat U=e^{-\frac{i}{\hbar}\hat Ht}$
> $\partial_t\hat U=-\frac{i}{\hbar}\hat He^{-\frac{i}{\hbar}\hat Ht}=-\frac{i}{\hbar}\hat H\hat U$

Why would we do it? Let's take a quick derivative:
> $\partial_t\hat A^{(H)}$
> $=\partial_t(\hat U^\dagger\hat A^{(s)}\hat U)$
> $=\partial_t\hat U^\dagger\hat A^{(s)}\hat U+\hat U^\dagger\partial_t\hat A^{(s)}\hat U+\hat U^\dagger\hat A^{(s)}\partial_t\hat U$
> $=\partial_t\hat U^\dagger\hat A^{(s)}\hat U+0+\hat U^\dagger\hat A^{(s)}\partial_t\hat U$
> $=\partial_t\hat U^\dagger\hat A^{(s)}\hat U+0+\hat U^\dagger\hat A^{(s)}\partial_t\hat U$
> $-\frac{i}{h}[\hat A^{(H)},\hat H]$

Schrodinger cares about the outside states, but the things are moving, but nothing happens to the operators. But Heisenberg cares about local stuff that moves but you don't, so you get fictitious forces, so the operators get transformed.

Let's consider another case: $\hat H$ is time-dependent but commutes with itself for all $t$.
> $\vec{B}=B_0(t)\hat \delta$
> $\hat H=-\vec{m}\cdot\vec{B}=mB_0(t)\sigma_\delta$

For an ordinary function $u(t,t_0)$:
> $\partial_tu(t,t_0)=f(t)u(t,t_0)$
> $u(t,t_0)=\exp\int_{t_0}^tdt\cdot f(t_1)$
> $\hat U=\exp[-\frac{i}{\hbar}\int dt\cdot\hat H]$

If $B_0$ is linear in time:
> $\vec{B}=b_0t\hat\delta$
> $\hat U=\exp[-\frac{i}{\hbar}\int dt\cdot mb_0t\sigma_\delta]$
> $\hat U=\exp[-\frac{i}{\hbar}mb_0\sigma_\delta\int dt\cdot t]$
> $\hat U=\exp[-\frac{i}{\hbar}mb_0\sigma_\delta\frac{1}{2}(t^2-t_0^2)]$
> $\hat U=e^{-\frac{i}{2\hbar}b_0(t^2-t_0^2)\sigma_\delta}$, $t>t_0$

The issue with this is that you get degeneracy at the origin and you won't be able to figure out how to time-evolve at that point. How would you progress?

Let's go back to solving the shits:
> $\partial_tU=\frac{1}{i\hbar}HU$, $U(t_0,t_0)=I$

The exponential solution fails in general, as the Hamiltonian does not commute in time.
> $U(t,t_0)=e^{\frac{1}{i\hbar}\int dtH(t)}=1+\frac{1}{i\hbar}\int dtH(t)+\frac{1}{2(i\hbar)^2}\int dtH(t)\int dtH(t)+\dots$
> $\partial_tU=0+\frac{1}{i\hbar}H(t)+\frac{1}{2(i\hbar)^2}[H(t)\cdot\int dtH(t)+\int dtH(t)\cdot H(t)]+\dots$