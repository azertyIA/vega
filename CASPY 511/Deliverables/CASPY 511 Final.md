## Q1. Angular Momentum
For the orbital angular momentum $\hat L=\hat r\times\hat p$ and the spin angular momentum $\hat S$; it should be noted that Sakurai sparsely mentioned that the Levi-Civita symbol should be summed over, but with that in mind you can extrapolate the following representation:  
$$\hat L_i=\Sigma\epsilon_{ijk}\hat r_j\hat p_k$$
$$[L_i,L_j]=i\hbar\epsilon_{ijk} L_k$$
i. Prove that $[\hat L_i,\hat p_j]=i\hbar\epsilon_{ijk}\hat p_k$.
> $[\hat L_i,\hat p_j]=[(\Sigma\epsilon_{i2k}\hat r_2\hat p_k),\hat p_{j}]$ 
> $=\Sigma\epsilon_{i2k}[\hat r_2\hat p_k,\hat p_{j}]$
> $=\Sigma\epsilon_{i2k}(\hat r_2[\hat p_k,\hat p_j]+[\hat r_2,\hat p_{j}]\hat p_k)$
> $=\Sigma\epsilon_{i2k}(0+[\hat r_2,\hat p_{j}]\hat p_k)$ (commutes except for $2=j\to i\hbar$)
> $=\epsilon_{ijk}(i\hbar\hat p_k)$
> $=\boxed{i\hbar\epsilon_{ijk}\hat p_k}$

ii. Given $L_\pm=L_x\pm iL_y$, prove that $[L_+,L_-]=2\hbar L_z$.
> $[L_+,L_-]=[L_x+iL_y,L_x-iL_y]$
> $=(L_x+iL_y)(L_x-iL_y)-(L_x-iL_y)(L_x+iL_y)$
> $=(L_x^2-iL_xL_y+iL_yL_x+L_y^2)-(L_x^2-iL_yL_x+iL_xL_y+L_y^2)$
> $=(-iL_xL_y+iL_yL_x)-(-iL_yL_x+iL_xL_y)$
> $=2i(-L_xL_y+L_yL_x)$
> $=-2i[L_x,L_y]$
> $=\boxed{2\hbar L_z}$

iii. Prove that $[L_-,L_z]=\hbar L_-$.
> $[L_-,L_z]=[L_x-iL_y,L_z]$
> $=[L_x,L_z]-i[L_y,L_z]$
> $=-i\hbar L_y+\hbar L_x$
> $=\boxed{\hbar L_-}$

iv. Consider the operator $\hat K=\hat L+2\hat S$; is $\hat K$ an angular momentum operator?
> $[\hat K_i,\hat K_j]=[\hat L_i+2\hat S_i,\hat L_j+2\hat S_j]$
> $=[\hat L_i+2\hat S_i,\hat L_j+2\hat S_j]$
> $=[\hat L_i,\hat L_j+2\hat S_j]+[2\hat S_i,\hat L_j+2\hat S_j]$
> $=[\hat L_i,\hat L_j]+[\hat L_i,2\hat S_j]+[2\hat S_i,\hat L_j]+[2\hat S_i,2\hat S_j]$
> $=[\hat L_i,\hat L_j]+0+0+[2\hat S_i,2\hat S_j]$
> $=i\hbar\epsilon_{ijk}(\hat L_k+4\hat S_k)\neq i\hbar\epsilon_{ijk}\hat K_k$
> **It is not an angular momentum operator.**
## Q2. Heisenberg and Dirac Interaction Pictures
Consider a time-independent Hamiltonian with an interaction $\hat H=\hat H_0+\hat V$, where $\hat V$ is an interaction term. $\hat A_S,\hat B_S,\hat C_S$ are given general time-independent operators that satisfy the following identity in the Schrodinger picture:
$$[\hat A_S,\hat B_S]=i\hat C_S$$
a. Prove that $[\hat A_I,\hat B_I]=i\hat C_I$ in the interaction picture.
> $[\hat A_I,\hat B_I]=[e^{i\hat H_0t/\hbar}\hat A_Se^{-i\hat H_0t/\hbar},e^{i\hat H_0t/\hbar}\hat B_Se^{-i\hat H_0t/\hbar}]$
> $=e^{i\hat H_0t/\hbar}\hat A_S\hat B_Se^{-i\hat H_0t/\hbar}-e^{i\hat H_0t/\hbar}\hat B_S\hat A_Se^{-i\hat H_0t/\hbar}$ (the adjacent conjugates cancel)
> $=e^{i\hat H_0t/\hbar}(\hat A_S\hat B_S-\hat B_S\hat A_S)e^{-i\hat H_0t/\hbar}$
> $=e^{i\hat H_0t/\hbar}[\hat A_S,\hat B_S]e^{-i\hat H_0t/\hbar}$
> $=e^{i\hat H_0t/\hbar}i\hat C_Se^{-i\hat H_0t/\hbar}$ (the given identity)
> $=\boxed{i\hat C_I}$

b. Show that the time evolution operator is described by $i\hbar\partial_t\hat A_I(t)=[\hat A_I(t),\hat H_0]$.
> $i\hbar\partial_t\hat A_I(t)=i\hbar\partial_t(e^{i\hat H_0t/\hbar}\hat A_Se^{-i\hat H_0t/\hbar})$
> $=i\hbar(\partial_te^{i\hat H_0t/\hbar}\hat A_Se^{-i\hat H_0t/\hbar})+i\hbar(e^{i\hat H_0t/\hbar}\hat A_S\partial_te^{-i\hat H_0t/\hbar})$
> $=i\hbar((i\hat H_0/\hbar)e^{i\hat H_0t/\hbar}\hat A_Se^{-i\hat H_0t/\hbar})+i\hbar(e^{i\hat H_0t/\hbar}\hat A_S(-i\hat H_0/\hbar)e^{-i\hat H_0t/\hbar})$
> $=-(\hat H_0e^{i\hat H_0t/\hbar}\hat A_Se^{-i\hat H_0t/\hbar})+(e^{i\hat H_0t/\hbar}\hat A_S\hat H_0e^{-i\hat H_0t/\hbar})$
> $=-(\hat H_0e^{i\hat H_0t/\hbar}\hat A_Se^{-i\hat H_0t/\hbar})+(e^{i\hat H_0t/\hbar}\hat A_Se^{-i\hat H_0t/\hbar}\hat H_0)$ ($[\hat H,f(\hat H)]=0$)
> $=-(\hat H_0\hat A_I(t))+(\hat A_I(t)\hat H_0)$
> $=\boxed{[\hat A_I(t),\hat H_0]}$
## Q3. Pauli Spin Matrices
Consider the Pauli Spin Matrices $\sigma$ and the $2\times2$ identity matrix $\mathbb 1$.

a. For any two $\vec v,\vec w$ prove that $(\vec v\cdot\sigma)(\vec w\cdot\sigma)=(\vec v\cdot \vec w)\mathbb1+i(\vec v\times\vec w)\cdot\sigma$. (Looks like geo. algebra!)
> $(\vec v\cdot\sigma)(\vec w\cdot\sigma)=(v_x\sigma_x+v_y\sigma_y+v_z\sigma_z)(w_x\sigma_x+w_y\sigma_y+w_z\sigma_z)$
> $=((v_x\sigma_xw_x\sigma_x+v_x\sigma_xw_y\sigma_y+v_x\sigma_xw_z\sigma_z)$
> $+(v_y\sigma_yw_x\sigma_x+v_y\sigma_yw_y\sigma_y+v_y\sigma_yw_z\sigma_z)$
> $+(v_z\sigma_zw_x\sigma_x+v_z\sigma_zw_y\sigma_y+v_z\sigma_zw_z\sigma_z))$
> $=((v_x\sigma_xw_x\sigma_x+v_y\sigma_yw_y\sigma_y+v_z\sigma_zw_z\sigma_z)$ (matching)
> $+(v_y\sigma_yw_z\sigma_z+v_z\sigma_zw_x\sigma_x+v_x\sigma_xw_y\sigma_y)$ (good chirality x -> y -> z -> x)
> $+(v_y\sigma_yw_x\sigma_x+v_z\sigma_zw_y\sigma_y+v_x\sigma_xw_z\sigma_z))$ (bad chirality x -> z -> y -> x)
> $=((v_xw_x+v_yw_y+v_zw_z)\mathbb1$ ($\sigma_i^2=\mathbb1$)
> $+i(v_yw_z\sigma_x+v_zw_x\sigma_y+v_xw_y\sigma_z)$ (good: $\sigma_i\sigma_j=i\sigma_k$)
> $-i(v_yw_x\sigma_z+v_zw_y\sigma_x+v_xw_z\sigma_y))$ (bad: $\sigma_j\sigma_i=-i\sigma_k$)
> $=(\vec v\cdot\vec w)\mathbb1+i((v_yw_z-v_zw_y)\sigma_x+(v_zw_x-v_xw_z)\sigma_y+(v_xw_y-v_yw_x)\sigma_z)$
> $=(\vec v\cdot\vec w)\mathbb1+i((v_yw_z-v_zw_y)\hat x+(v_zw_x-v_xw_z)\hat y+(v_xw_y-v_yw_x)\hat z)\cdot \sigma$
> $=\boxed{(\vec v\cdot \vec w)\mathbb1+i(\vec v\times\vec w)\cdot\sigma}$

b. Prove that $[\vec v\cdot\sigma,\vec w\cdot\sigma]=2i(\vec v\times\vec w)\cdot\sigma$
> $[\vec v\cdot\sigma,\vec w\cdot\sigma]=(\vec v\cdot\sigma)(\vec w\cdot\sigma)-(\vec w\cdot\sigma)(\vec v\cdot\sigma)$
> $=((\vec v\cdot \vec w)\mathbb1+i(\vec v\times\vec w)\cdot\sigma)-((\vec w\cdot \vec v)\mathbb1+i(\vec w\times\vec v)\cdot\sigma)$
> $=(0)\mathbb1+i(\vec v\times\vec w-\vec w\times\vec v)\cdot\sigma$
> $=\boxed{2i(\vec v\times\vec w)\cdot\sigma}$ (cross product is anticommutative)
## Q4. Degeneracies in the Harmonic Oscillator
Consider the Harmonic Oscillator in 1D and in 3D. The energy is a monochromatic $\frac72\hbar\omega_0$. $$\hat H_1=\frac1{2m}\hat p^2_x+\frac12m\omega_0^2\hat x^2\;\;\;\;\;\;\;\;\;\hat H_3=\frac1{2m}\hat p^2+\frac12m\omega_0^2\hat r^2$$i. What is the degeneracy of the $\frac72\hbar\omega_0$ state in 1D?
> $\hbar\omega_0(n+\frac12)=\frac72\hbar\omega_0$
> Just the one. (n=3)

ii. What is the degeneracy of the $\frac72\hbar\omega_0$ state in 1D?
> $\hbar\omega_0(n_x+n_y+n_z+\frac32)=\frac72\hbar\omega_0$
> $n_x+n_y+n_z=2$
> Six degeneracies: (200, 020, 002, 011, 101, 110)

Assume that the particle is spinless with charge $q$ under a weak uniform electric field $\vec E=E_0\hat x$. 
> $\hat H'_1=\frac1{2m}\hat p_x^2+\frac12m\omega_0^2\hat x^2+E_0q\hat x\to$ centered at a different place
> $\hat H'_3=\frac1{2m}\hat p^2+\frac12m\omega_0^2\hat r^2+E_0q\hat x\to$ also centered at a different place, but changed in the x axis
> It's a weird question to ask because it's likely true that the $\frac72\hbar\omega_0$ eigenstate doesn't exist now since its perturbed by the E-field as a constant term (when you shift each to its proper center). But for the benefit of the doubt I'll assume its talking about the nearby states.

iii. How has the degeneracy changed for the 1D case?
> degeneracy shouldn't change, the center just shifts

iv. How has the degeneracy changed for the 3D case?
> degeneracy should decrease, as you lose symmetries, and degeneracies would split on their differences in x (i.e. between x-y, and x-z).
## Q5. Wigner-Eckhart Theorem: Balmer Transition
Students need to analyze the Hydrogen atom electric dipole transition spectral line 3d (not f) -> 2p. Each of your students is asked to identify one valid transition from an initial state to a final state listed below, for which the probability of the transition is not zero, or for which the transition matrix element is non-zero. 
$$\ket{n=3,l=2,m_l}\to\ket{n'=2,l'=1,m_l'}$$
i. Alfie: $m_l=-1\to m_l'=-1$ CG ***non-zero, works***
ii. Betty: $m_l=2\to m_l'=0$ CG zero doesn't work
iii. Gammy: $m_l=2\to m_l'=-1$ CG zero doesn't work
iv. Delter: $m_l=2\to m_l'=1$ CG ***non-zero works***
v. Epsom: $m_l=-2\to m_l'=-3$ CG zero doesn't work
> **Only Alfie's and Delter's transitions work, but I'd double check Delter's with Timucin's paper.**
![[Pasted image 20251217055129.png]]
## L1. Charge-Flux Correlation
Consider the quantized linear LC circuit described by the Hamiltonian, with capacitance and inductance. The time dependent magnetic flux and charge operators can be rewritten in the Heisenberg picture with $\hat A_H(t)=e^{i\hat Ht/\hbar}\hat Ae^{-i\hat Ht/\hbar}$.
$$\hat H=\frac1{2C}\hat Q^2+\frac L2\hat \Phi^2$$
$$\hat Q=i\Delta_Q(\hat a^\dagger-\hat a)$$
$$\hat \Phi=\Delta_\Phi(\hat a^\dagger+\hat a)$$
a. Find the expectation value of the commutator $\braket{0|[\hat\Phi_H(0),\hat Q_H(t)]|0}$:
> $\braket{0|[\hat\Phi_H(0),\hat Q_H(t)]|0}=\braket{0|[\hat\Phi,e^{i\hat Ht/\hbar}\hat Qe^{-i\hat Ht/\hbar}]|0}$
> $=i\Delta_Q\Delta_\Phi\braket{0|[\hat a^\dagger+\hat a,e^{i\hat Ht/\hbar}(\hat a^\dagger-\hat a)e^{-i\hat Ht/\hbar}]|0}$
> $=i\Delta_Q\Delta_\Phi\braket{0|[\hat a^\dagger+\hat a,\hat a_H^\dagger(t)-\hat a_H(t)]|0}$
> $\hat a_H(t)=e^{-i\omega t}\hat a_H(0)=e^{-i\omega t}\hat a$ (from HW 7) $\omega$ can be inferred to be based on LC
> $\hat a^\dagger_H(t)=e^{i\omega t}\hat a_H^\dagger(0)=e^{i\omega t}\hat a^\dagger$ (from HW 7)
> $=i\Delta_Q\Delta_\Phi\braket{0|[\hat a^\dagger+\hat a,e^{i\omega t}\hat a^\dagger-e^{-i\omega t}\hat a]|0}$
> $=i\Delta_Q\Delta_\Phi\braket{0|[\hat a^\dagger,e^{i\omega t}\hat a^\dagger-e^{-i\omega t}\hat a]+[\hat a,e^{i\omega t}\hat a^\dagger-e^{-i\omega t}\hat a]|0}$
> $=i\Delta_Q\Delta_\Phi\braket{0|-[\hat a^\dagger,e^{-i\omega t}\hat a]+[\hat a,e^{i\omega t}\hat a^\dagger]|0}$
> $=i\Delta_Q\Delta_\Phi\braket{0|-e^{-i\omega t}[\hat a^\dagger,\hat a]+e^{i\omega t}[\hat a,\hat a^\dagger]|0}$
> $=i\Delta_Q\Delta_\Phi\braket{0|e^{-i\omega t}+e^{i\omega t}|0}$
> $=i\Delta_Q\Delta_\Phi\braket{0|2\cos(\omega t)|0}$
> $=\boxed{2i\Delta_Q\Delta_\Phi\cos(\omega t)=i\hbar\cos(\omega t),\omega=1/\sqrt{LC}}$

b. Now consider this Coherent state for this LC circuit defined as the eigenstate of $\hat a$:
$$\hat a\ket\alpha=\alpha\ket\alpha$$
$$(\hat a\ket\alpha)^\dagger=\bra\alpha\hat a^\dagger=\bra\alpha\alpha^*$$
i. Express the expectation values of the charge on operator $\braket{\alpha|\hat Q_H(t)|\alpha}$ in terms of $\alpha,C,L$.
> $\braket{\alpha|\hat Q_H(t)|\alpha}=i\Delta_Q\braket{\alpha|e^{i\omega t}\hat a^\dagger-e^{-i\omega t}\hat a|\alpha}$
> $=i\Delta_Q\braket{\alpha|e^{i\omega t}\hat a^\dagger-e^{-i\omega t}\hat a|\alpha}$
> $=i\Delta_Q\braket{\alpha|e^{i\omega t}\alpha^*-e^{-i\omega t}\alpha|\alpha}$
> $=i\sqrt{\frac{C\hbar\omega_0}2}(e^{i\omega t}\alpha^*-e^{-i\omega t}\alpha)$
> $=\boxed{\sqrt{2\hbar\sqrt{C/L}}Im[\alpha e^{-it/\sqrt{LC}}]}$

ii. Show that the expectation value satisfies the classical LC circuit equation of motion for the charge stored by the capacitor that you would have learned in first-year Physics. (I did not take the coefficients with me.)
> $Q=CV,V=-L\ddot Q$
> $Q=(-LC)\ddot Q$
> $-Im[\alpha e^{-it/\sqrt{LC}}]/LC=\partial_t^2Im[\alpha e^{-it/\sqrt{LC}}]$
> $=Im[\alpha\partial_t^2 e^{-it/\sqrt{LC}}]$
> $=Im[\alpha(-1/LC) e^{-it/\sqrt{LC}}]$
> $=-Im[\alpha e^{-it/\sqrt{LC}}]/LC$
> **The expectation value fits the equation of motions from classical E&M.**

c. Find the expectation value of the commutator $\braket{\alpha|[\hat\Phi_H(0),\hat Q_H(t)]|\alpha}$:
> **Part (a) did not see any impact from the $\ket0$. The result was achieved as a direct result of the commutator. Changing that 0 to a coherent state won't do anything because it's a superposition of Fock states regardless.**
> $=\boxed{2i\Delta_Q\Delta_\Phi\cos(\omega t)=i\hbar\cos(\omega t),\omega=1/\sqrt{LC}}$

d. For the special case when $t=0$, do a sanity check by comparing your answer in part (c) with your answer in part (a).
> $[\hat\Phi_H(0),\hat Q_H(0)]=[\hat\Phi,\hat Q]$
> $=i\hbar\cos(\omega(0))=\boxed{i\hbar}$
> **Parts (a) and (c) should be the same. It's interesting to note that bringing t=0 returns the expected value to the canonical commutator, granting the minimum possible uncertainty. At other points in t, we would get values smaller than this uncertainty, but the operators at play are taken at different times. Thus, this tells us how "correlated" (stole from question title) the charge and flux operators are across time.**
## L2. Scattering With Two Delta Things :)
A monochromatic neutron beam with wavelength $\lambda_D=\lambda$ is incident along the z-axis ($\vec k_0=k_0\hat z$) on a non-magnetic molecule oriented such that two delta things are separated by distance $d$ on the y-axis. The potential for such with parameter $V_0b^3$ is:
$$V(\vec r')=V_0b^3\delta(x')\delta(z')[\delta(y'-\frac d2)+e^{i\beta}\delta(y'+\frac d2)]$$
a. Fourier Transform $V(\vec r')\to V_q(\vec q)$.
> $V_q(\vec q)=\iiint d\vec r'e^{-i\vec q\cdot\vec r'}V(\vec r')$
> $=V_0b^3\iiint d\vec r'e^{-i\vec q\cdot\vec r'}\delta(x')\delta(z')[\delta(y'-\frac d2)+e^{i\beta}\delta(y'+\frac d2)]$
> $=V_0b^3\iiint d\vec r'[e^{-i\vec q\cdot\vec r'}\delta^3(\vec r'-\frac d2\hat y)+e^{-i\vec q\cdot\vec r'}e^{i\beta}\delta^3(\vec r'+\frac d2\hat y)]$
> $=V_0b^3[e^{-i\vec q\cdot\frac d2\hat y}+e^{+i\vec q\cdot\frac d2\hat y+i\beta}]$ (delta function selection)
> $=V_0b^3[e^{-id\vec q\cdot\hat y/2}+e^{+id\vec q\cdot\hat y/2+i\beta}]$
> $\vec q\cdot\hat y=q_y=k_0(\hat r-\hat z)\cdot\hat y=y=k_0\sin\theta\sin\phi$
> $=V_0b^3e^{+i\beta/2}[e^{-i(dk_0\sin\theta\sin\phi+\beta)/2}+e^{+i(dk_0\sin\theta\sin\phi+\beta)/2}]$
> $=\boxed{2V_0b^3e^{+i\beta/2}\cos((dk_0\sin\theta\sin\phi+\beta)/2)}$

b. In the first Born approximation, calculate (it looks funny but I think it's really cool) $\partial_\Omega\sigma$.
> $\psi(\vec r)=\psi_0(r)+\frac{2m}{\hbar^2}\iiint d\vec r'G(\vec r-\vec r')V(\vec r')\psi(\vec r')$, $G(\vec R)=\frac{-e^{ik_0R}}{4\pi R}$
> $\psi^{(0)}(\vec r)=\psi_0(\vec r)=e^{ik_0z}$
> $\psi^{(1)}(\vec r)=\psi_0(r)+\frac{2m}{\hbar^2}\iiint d\vec r'G(\vec r-\vec r')V(\vec r')\psi^{(0)}(\vec r')$
> $=e^{ik_0z}+\frac{2m}{\hbar^2}\iiint d\vec r'\frac{-e^{ik_0|\vec r-\vec r'|}}{4\pi|\vec r-\vec r'|}V(\vec r')e^{ik_0z'}$
> $=e^{ik_0z}-\frac{m}{2\pi\hbar^2}\iiint d\vec r'\frac{1}{|\vec r-\vec r'|}e^{ik_0|\vec r-\vec r'|}V(\vec r')e^{ik_0z'}$
> $=e^{ik_0z}-\frac{m}{2\pi\hbar^2}\iiint d\vec r'\frac{1}{r}e^{ik_0(r-\hat r\cdot\vec r')}V(\vec r')e^{ik_0z'}$ (a lot of approximating)
> $=e^{ik_0z}-\frac{m}{2\pi\hbar^2r}e^{ik_0r}\iiint d\vec r'V(\vec r')e^{ik_0(\hat z-\hat r)\cdot\vec r'}$
> $=e^{ik_0z}-\frac{m}{2\pi\hbar^2r}e^{ik_0r}\iiint d\vec r'V(\vec r')e^{-i\vec q\cdot\vec r'}$ (last term is a FT)
> $=e^{ik_0z}-\frac{e^{ik_0r}}r\frac{m}{2\pi\hbar^2}V_q(\vec q)=e^{ik_0z}+\frac{e^{ik_0r}}rf(\theta,\phi)$

> $\partial_\Omega\sigma=|f(\theta,\phi)|^2=\frac{m^2}{4\pi^2\hbar^4}|V_q(\vec q)|^2$
> $=\frac{V_0^2b^6m^2}{\pi^2\hbar^4}|e^{+i\beta/2}\cos((dk_0\sin\theta\sin\phi+\beta)/2)|^2$
> $=\boxed{\frac{V_0^2b^6m^2}{\pi^2\hbar^4}\cos^2(dk_0\sin\theta\sin\phi/2+\beta/2)}$

c. Given an observer far away on the x-axis, do they see a bright spot or dark spot?
> $\hat r=\hat xL\to1=\cos\phi\sin\theta$
> $\theta=\pi/2,\phi=0$
> $\partial_\Omega\sigma=\frac{V_0^2b^6m^2}{\pi^2\hbar^4}\cos^2(dk_0\sin\theta\sin\phi/2+\beta/2)$
> $=\frac{V_0^2b^6m^2}{\pi^2\hbar^4}\cos^2(\beta/2)$
> **There isn't enough information unless $\beta$ is known...**

d. The energy of the neutron has been tuned such that $k=2\pi/\lambda=4\pi/d$ and $\beta=\pi/4$. Plot $\partial_\Omega\sigma$.
> $=\frac{V_0^2b^6m^2}{\pi^2\hbar^4}\cos^2(2\pi\sin\theta\sin\phi+\pi/8)$
### Plots of $\partial_\Omega\sigma=|f(\theta,\phi)|^2$ (Mathematica)
![[Pasted image 20251217060638.png]]![[Pasted image 20251217060658.png]]
*The following is $\partial_\Omega\sigma$ which is fairly asymmetric given the $\pi/8$ phase. As a result, you have two different ends to this "plunger" shape. As can be seen, the constant scaling coefficients has been omitted from the graph for ease of reading. It matters relatively anyways, and cosine squared doesn't go beyond 1.
## L3. Teleportation Protocol
Consider the following Bell entangled state listed below. Suppose Alice and Bob use this state for teleporting Alice's qubit to Bob. Alice and Bob cannot transfer the complex coefficients, but they can send classical bits of information.
$$\ket{\Psi_{AB}}=\frac1{\sqrt2}(\ket{0_A}\otimes\ket{1_B}+\ket{1_A}\otimes\ket{0_B})$$
$$\ket{\phi_i}=\alpha\ket{0_i}+\beta\ket{1_i}\to\alpha\ket{0_f}+\beta\ket{1_f}=\ket{\phi_f}$$
**Step 0:** Alice entangles her qubit with the shared Bell state, performing a CNOT (XOR) operation which takes both qubits. (Flip just the A if the initial bit is 1)
> $\ket{\phi_i}\otimes\ket{\Psi_{AB}}=\ket{\phi_i,\Psi_{AB}}$
> $=\frac1{\sqrt2}(\alpha\ket{0_i}+\beta\ket{1_i})\otimes(\ket{0_A,1_B}+\ket{1_A,0_B})$
> $=\frac1{\sqrt2}(\alpha\ket{0_i,0_A,1_B}+\alpha\ket{0_i,1_A,0_B}+\beta\ket{1_i,0_A,1_B}+\beta\ket{1_i,1_A,0_B})$ (now do the CNOT)
> $\ket{\Phi_{iAB}}=\frac1{\sqrt2}(\alpha\ket{0_i,0_A,1_B}+\alpha\ket{0_i,1_A,0_B}+\beta\ket{1_i,1_A,1_B}+\beta\ket{1_i,0_A,0_B})$

**Step 1:** Alice performs a Hadamard transformation on the input qubit (the one used to flip hers). The Hadamard turns 0 to even 0 + 1 and 1 to 0 - 1.
> $\hat H\ket{\Phi_{iAB}}=\frac12(\alpha\ket{+_i,0_A,1_B}+\alpha\ket{+_i,1_A,0_B}+\beta\ket{-_i,1_A,1_B}+\beta\ket{-_i,0_A,0_B})$
> $=\frac12(\alpha\ket{0_i,0_A,1_B}+\alpha\ket{1_i,0_A,1_B}$
> $+\alpha\ket{0_i,1_A,0_B}+\alpha\ket{1_i,1_A,0_B}$
> $+\beta\ket{0_i,1_A,1_B}-\beta\ket{1_i,1_A,1_B}$
> $+\beta\ket{0_i,0_A,0_B}-\beta\ket{1_i,0_A,0_B})$
> $=\frac12(\beta\ket{0_i,0_A,0_B}+\alpha\ket{0_i,0_A,1_B}$
> $+\alpha\ket{0_i,1_A,0_B}+\beta\ket{0_i,1_A,1_B}$
> $-\beta\ket{1_i,0_A,0_B}+\alpha\ket{1_i,0_A,1_B}$
> $+\alpha\ket{1_i,1_A,0_B}-\beta\ket{1_i,1_A,1_B})$

> $=(\ket{0_i,0_A}\otimes\frac12(+\beta\ket{0_B}+\alpha\ket{1_B})$
> $+(\ket{0_i,1_A}\otimes\frac12(+\alpha\ket{0_B}+\beta\ket{1_B})$
> $+(\ket{1_i,0_A}\otimes\frac12(-\beta\ket{0_B}+\alpha\ket{1_B})$
> $+(\ket{1_i,1_A}\otimes\frac12(+\alpha\ket{0_B}-\beta\ket{1_B})$

**Step 2:** Alice performs a measurement and calls Bob to tell him what operator to use given what she had measured.
> $\ket{0_i0_A}\to$ the coefficients are flipped so use **Pauli-X**.
> $\ket{0_i1_A}\to$ the coefficients are fine so use Nothing (**I**).
> $\ket{1_i0_A}\to$ $\beta$ is negative and in wrong place so use **Pauli-Z after Pauli-X**.
> $\ket{1_i1_A}\to$ only $\beta$ is negative so use **Pauli-Z**.

It is important to note you could also use a (negative or positive) Pauli-Y for the 10 case, but you lose global phase, which is usually irrelevant anyways.