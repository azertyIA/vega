In order to solve more intricate equations of motions as a result of [[QM Axiom II]] that [[Schrodinger and Heisenberg Pictures]] cannot do easily, Dirac smushed the two pictures into one. 

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