The Schrodinger picture is the equation we've been learning:
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
## Dirac Interaction Picture

If they do not commute, then it will never work out. So the actual general solution can be written in terms of the Dyson Series, which can be proven in a similar way as the pictures.
> $H(t)=H_0+V(t)$, some time independent part and some interaction.

Case 1 exists when $H_0$ is the only term. We know how to solve this part. 

Define $\Psi_I(t)$ in terms of the Schrodinger picture $\Psi(t_0)$:
> $\ket{\Psi_I,t}=e^{+\frac{i}{\hbar}H_0(t-t_0)}\ket{\Psi,t}$
> $\ket{\Psi,t}=e^{-\frac{i}{\hbar}H_0(t-t_0)}\ket{\Psi_I,t}$
> $\ket{\Psi_I,t=t_0}=\ket{\Psi(t_0)}$

So we need some new operator for this new interaction picture:
> $\ket{\Psi_I,t}=U_I\ket{\Psi_I,t_0}$

Let's try to get some information about $\partial_tU_I$ (equation of motion) from $U$:
> $\ket{\Psi_I,t}=e^{+\frac{i}{\hbar}H_0(t-t_0)}U(t,t_0)\ket{\Psi,t_0}$
> $\ket{\Psi_I,t}=e^{+\frac{i}{\hbar}H_0(t-t_0)}U(t,t_0)\ket{\Psi_I,t_0}$ (The initial states are the same)

So the entire operator of $U_I$ is clear:
> $U_I=e^{+\frac{i}{\hbar}H_0(t-t_0)}U(t,t_0)$
> $U=e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I(t,t_0)$

Now the derivative:
> $\partial_tU_I=\partial_te^{+\frac{i}{\hbar}H_0(t-t_0)}U+e^{+\frac{i}{\hbar}H_0(t-t_0)}\partial_tU$
> $=\frac{i}{\hbar}H_0e^{+\frac{i}{\hbar}H_0(t-t_0)}U+e^{+\frac{i}{\hbar}H_0(t-t_0)}\frac{1}{i\hbar}HU)$
> $=\frac{i}{\hbar}H_0e^{+\frac{i}{\hbar}H_0(t-t_0)}U+e^{+\frac{i}{\hbar}H_0(t-t_0)}\frac{1}{i\hbar}(H_0+V(t))U$
> $=\frac{i}{\hbar}H_0e^{+\frac{i}{\hbar}H_0(t-t_0)}e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I+e^{+\frac{i}{\hbar}H_0(t-t_0)}\frac{1}{i\hbar}(H_0+V(t))e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I$
> $=\frac{i}{\hbar}H_0U_I+e^{+\frac{i}{\hbar}H_0(t-t_0)}\frac{1}{i\hbar}(H_0+V(t))e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I$
> $=\frac{i}{\hbar}H_0U_I+\frac{-i}{\hbar}e^{+\frac{i}{\hbar}H_0(t-t_0)}(H_0+V(t))e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I$
> $=\frac{i}{\hbar}H_0U_I+\frac{-i}{\hbar}e^{+\frac{i}{\hbar}H_0(t-t_0)}H_0e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I+\frac{-i}{\hbar}e^{+\frac{i}{\hbar}H_0(t-t_0)}V(t)e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I$ ($H_0$ self-commutes)
> $=\frac{i}{\hbar}H_0U_I+\frac{-i}{\hbar}H_0U_I+\frac{-i}{\hbar}e^{+\frac{i}{\hbar}H_0(t-t_0)}V(t)e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I$
> $=\frac{1}{i\hbar}e^{+\frac{i}{\hbar}H_0(t-t_0)}V(t)e^{-\frac{i}{\hbar}H_0(t-t_0)}U_I$ (define most of this as $V_I(t)$)
> $=\frac{1}{i\hbar}V_I(t)U_I(t)$

Now we got a brand new equation of motion:
> $\partial_tU_I=\frac{1}{i\hbar}V_I(t)U_I(t)$, where $V_I=e^{+\frac{i}{\hbar}H_0(t-t_0)}Ve^{+\frac{i}{\hbar}H_0(t-t_0)}$

Now let's integrate it with the initial time being $t_0$:
> $U_I(t,t_0)=U_I(t_0,t_0)+\frac{1}{i\hbar}\int dtV_I(t)U_I(t)$, the first term is just 1.
> $U_I(t,t_0)=1+\frac{1}{i\hbar}\int dtV_I(t)U_I(t)$

If $U_I$ can be 1, what if it was just always 1.
> $U^0_I=1$
> $U^1_I=1+\frac{1}{i\hbar}\int dtV_I(t)U_I^0(t)$
> $=1+\frac{1}{i\hbar}\int dtV_I(t)$
> $U^2_I=1+\frac{1}{i\hbar}\int dtV_I(t)U_I^1(t)$
> $=1+\frac{1}{i\hbar}\int dtV_I(t)(1+\frac{1}{i\hbar}\int dtV_I(t))$
> $=1+\frac{1}{i\hbar}\int dtV_I(t)+(\frac{1}{i\hbar})^2\int dtV_I(t)\int dtV_I(t)$
> $U_I=\Sigma_0(\frac{1}{i\hbar}\int_{t_0}^{t_{n+1}} dt_nV_I(t_n))^n$ (in the worst notation possible)

These are called "path ordered," but really it should be "time ordered." This is also known as the Dyson series. Oh, it's just a path integral. Trying to draw this out as a region for handling this many integrals gets you this wedge shape. As long as $t>t_n>t_{n-1}$.

This approach is important in path integrals, QFT, relativistic models, and multi-particle systems. These also lead to Feynman diagrams. The operator approach is more powerful than the state vector approach even in statistical mechanics.

If you truncate for computation, unitarity doesn't hold depending on the order.