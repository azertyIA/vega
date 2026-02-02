Gauge invariance:
> $\vec E=-\nabla\Phi-\partial_t\vec A$
> $\vec B=\nabla\times\vec A$

Imagine a field with $\vec B=B_0\hat z$
> $\nabla\times A=\hat e_z(\partial_xA_y-\partial_yA_x)$

There are many possibilities for such a potential:
> $\vec A=(-B_0y,B_0x,0)$
> $\vec A=(0,B_0x,0)$
> $\vec A=(-B_0y,0,0)$

Given:
> $U=e^{+iq\Lambda(\vec r,t)/\hbar}$
> $U^\dagger=e^{-iq\Lambda(\vec r,t)/\hbar}$

We need a few properties:
1. Unitarity (norm conservation)
2. Position invariance
3. Momentum invariance

Is this unitary? Well obviously, it's just a complex exponential.
> $\ket{a'}=U\ket a$
> $\braket{a'|a'}=\braket{a'|U^\dagger U|a'}=\braket{a|a}=1$

In PY511, we only call for time independent potentials only. ($\Lambda(x,t)=\Lambda(x)$)
> $\braket{a'|\vec x|a'}=\braket{a|\vec x|a}$
> $\braket{a|U^\dagger\vec xU|a}=\braket{a|\vec x|a}$
> $\vec x$ must commute with $U$.

What about momentum?
> $\vec p=-i\hbar\vec\nabla$
> $\braket{a'|\vec p|a'}=?$ given $\braket{a|\vec p|a}$
> $=\braket{a|U^\dagger\vec pU|a}$
> $=-i\hbar\braket{a|U^\dagger\vec\nabla (U|a})$
> $=q\braket{a|U^\dagger\vec \nabla\Lambda(\vec x)U|a}-i\hbar\braket{a|U^\dagger U\nabla|a}$
> $=q\braket{a|U^\dagger\vec \nabla\Lambda(\vec x)U|a}-i\hbar\braket{a|\vec p|a}$

So we need a gauge invariant momentum. $\vec p$ sucks. But $\vec p-q\vec A$ isn't. $\vec A$ can change by an amount $\Lambda$ anywhere. This is the definition of gauge invariance.
> $\braket{a'|\vec p-q\tilde A|a'}=?$ given $\braket{a|\vec p-q\vec A|a}$
> $=\braket{a|U^\dagger(\vec p-q\tilde A)U|a}$
> $\to U^\dagger(\vec p-q\tilde A)U=\vec p-q\vec A$
> $= U^\dagger(\vec p)U-U^\dagger(q\vec A(x))U-U^\dagger(q\nabla\Lambda)U$
> $= U^\dagger(\vec p)U-q\vec A(x)-q\nabla\Lambda$ (A is a function of x and commutes)
> $= U^\dagger[\vec p,U]+U^\dagger U\vec p-q\vec A(x)-q\nabla\Lambda$
> $= U^\dagger[\vec p,\vec x](iq(\nabla\Lambda)U/\hbar)+\vec p-q\vec A(x)-q\nabla\Lambda$
> $= q(\nabla\Lambda)U^\dagger U+\vec p-q\vec A(x)-q\nabla\Lambda$
> $= q\nabla\Lambda+\vec p-q\vec A(x)-q\nabla\Lambda$
> $=\vec p-q\vec A(x)$

The square should also be invariant. So the energy using this momentum operator should be invariant as well.
>$p^2/2m\to\frac1{2m}(\vec p-q\vec A)^2+q\Phi$

Gauge invariance:
> $\vec E=-\nabla\Phi-\partial_t\vec A$
> $\vec B=\nabla\times\vec A$

Non relativistic classical tells us that:
> $m\partial_t\vec v=q(\vec E+q\vec v\times\vec B)$
> $=q(-\nabla\Phi-\partial_t\vec A+\vec v\times(\nabla\times\vec A))$
> $=q(-\nabla\Phi-\partial_t\vec A+\vec v\times(\nabla\times\vec A))$
> $\partial_t(m\vec v+q\vec A)=q(-\nabla\Phi+\vec v\times(\nabla\times\vec A))$
> $=-q\nabla(\Phi-\vec v\cdot\vec A)$

The $i$ to change to a different thing is to represent a rotation.
> $L=mv^2/2-q(\Phi-\vec v\cdot\vec A)$
> $H=\vec p\cdot\vec v-mv^2/2+q(\Phi-\vec v\cdot\vec A)$
> $H=(\vec p-q\vec A)^2/2m+q\Phi$

If HUP is true: $[\vec x,\vec p]=i\hbar$
> $[\vec x,\vec p-q\vec A(\vec x)]=i\hbar$

So now we have some replacements to make for momentum and energy:
> $\tilde A=A+\nabla\Lambda$
> $\tilde\Phi=\Phi+\partial_t\Lambda$
> $\vec p\to\vec p-q\vec A$ ("pee momentum" to "em-vee momentum")
> $E\to E+q\Phi$

Imagine a square with some homogeneous magnetic field. Let's say this is a box and the particle could be looped from one edge to the opposite edge.
> $(x,y)=(x+nL_x,y+mL_y)$

> $\nabla\cdot\vec D=\rho=0$
> $\nabla\times\vec E=-\partial_tB=0$
> $\nabla\cdot\vec B=0$
> $\nabla\times\vec H=\vec J_C+\partial_t D=0$

Using gauge invariance:
> $\vec B=\nabla\times\vec A=B_0\hat z$
> $\vec A=(0,B_0x,0)$ is a possible answer

> $A_y(x,y)=A_y(x,y+L_y)$
> $B_0x=B_0x$

> $A_y(x,y)=A_y(x+L_x,y)$
> $B_0x\neq B_0(x+L_x)$

Let's now try $\tilde A(x+L_x,y)=A_y(x,y)+\partial_y\Lambda$
> $(x+L_x)B_0=xB_0+\partial_y\Lambda$
> $\Lambda=B_0L_xy$

Going to QM:
> $\tilde\psi(x,y)=e^{+iq\Lambda(x,y)/\hbar}\psi(x,y)$
> $\tilde\psi(x,L_y)=\tilde\psi(x,0)$?
> $e^{+iq\Lambda(x,L_y)/\hbar}\psi(x,L_y)=\psi(x,0)$
> $e^{+iqB_0L_xL_y/\hbar}\psi(x,L_y)=\psi(x,0)$
> $e^{+iqB_0L_xL_y/\hbar}\psi(x,0)=\psi(x,0)$
> $e^{+iqB_0L_xL_y/\hbar}=1$
> $qB_0L_xL_y/\hbar=2\pi n$
> $q\Phi_B/\hbar=2\pi n$
> $\Phi_B=nh/q$ ($q$ should be the electron charge)

Magnetic flux is quantized. The SI units for flux quantum has an additional half term because at the time, they did measurements in a superconductor where electrons are paired and entangled, having a charge twice more.
> $\Phi_0=nh/2q=2\times10^{-15}\text{ T-m}^2/\text{Wb}=1\text{ Mx}$ 

Meisner effect is to blame here.

Let's take a random cyclotron.
> $\hat H=\hat p/2m$
> $H=i\hbar\partial_t=(\vec p-q\vec A)^2+q\Phi$
> $=p^2+(qA)^2+\vec p\cdot(q\vec A)+q\vec A\cdot\vec p+q\Phi$

Putting a weird phase thing switches vectors to tildes.

> $L(\vec x,\vec v,t)=\frac12mv^2-q\Phi+q\vec v\cdot \vec A$

Given a closed loop:
> $1=\braket{x_1,t_1|x_2,t_2}=\braket{x_1,t_1|e^{i\int dtL(x,\dot x,t)/\hbar}|x_1,t_1}$
> $=e^{i\int dtL(x,\dot x,t)/\hbar}\braket{x_1,t_1|x_1,t_1}=1$
> $=e^{i\int dtL(x,\dot x,t)/\hbar}=1$
> $=e^{iq\int dt\vec v\cdot\vec A/\hbar}=1$
> $=q/\hbar\int dt\vec v\cdot\vec A=2\pi n$
> $=\int dt\vec v\cdot\vec A=hn/e$
> $=\oint d\vec l\cdot\vec A$
> $=\iint d\vec n\cdot(\nabla\times\vec A)$
> $=\iint d\vec n\cdot\vec B$
> $=\Phi_B=hn/e$

We need to solve the Schrodinger equation somehow.
> $\hat H\ket\Psi=i\hbar\partial_t\ket\Psi$
> $=\text{painful to write}$

But we can get a little more clever if $\Phi=0$:
> $=\frac1{2m}[(\hat p_x)^2+(\hat p_y-qB_0x)^2]\ket{\Psi,x,y}=i\hbar\partial_t\ket{\Psi,x,y}$ (no y in there at all)
> $=\ket{\Psi,x,y}=e^{ik_yy}\ket{\psi,x}$
> ...given $\hat p_y=\hbar\hat k_y$.

Because $\hat p_y$ and $\hat H$ commute, you can create an eigenstate that is simultaneous of both opertors.
> $\hat H\ket{\epsilon_n,k_y}=\epsilon_n\ket{\epsilon_n,k_y}$
> $\hat p_y\ket{\epsilon_n,k_y}=\hbar k_y\ket{\epsilon_n,k_y}$

So if you have a function of the operator next to its eigenstate, you can just replace the parameter with the eigenvalue.
> $f(\hat k_y)\ket{\epsilon_n,k_y}$
> $=\Sigma c_i\hat k^i_y\ket{\epsilon_n,k_y}$
> $=\Sigma c_ik^i_y\ket{\epsilon_n,k_y}$
> $=f(k_y)\ket{\epsilon_n,k_y}$

So with the Hamiltonian in mind:
> $=\frac1{2m}[(\hat p_x)^2+(\hbar k_y-qB_0x)^2]\ket{\Psi,x,y}=i\hbar\partial_t\ket{\Psi,x,y}$
> $=\frac1{2m}[(\hat p_x)^2+(qB_0)^2(x-\hbar k_y/qB_0)^2]\ket{\Psi,x,y}=i\hbar\partial_t\ket{\Psi,x,y}$
> $=\frac1{2m}\hat p_x^2+\frac1{2m}(qB_0)^2(x-\hbar k_y/qB_0)^2=i\hbar\partial_t$

If $x_B=\hbar k_y/qB_0=\hbar k_y/m\omega$:
> $=\frac1{2m}\hat p_x^2+\frac12m\omega^2(x-x_B)^2=i\hbar\partial_t$
> It's a harmonic oscillator.

Conductance ($G$ in Siemens) is related to quantization by:
> $G=1/R_{xy}=n_Qe^2/\hbar$

The classical Hall Effect has a magnetic field in a steady state in the z direction and an electric field in the y direction. You can then select a velocity to move in a straight line given $v=E_0/B_0$.

The 2D current density is thusly $\hat J=-ne\vec v=\int d\vec a\cdot\vec J=newE_0/B_0$. The hall potential is $\int d\vec l\cdot\vec E=E_0w$ So the resistance must be $B_0/ne$. The longitudinal resistance is $(L/W\mu)(1/ne^2)$.



