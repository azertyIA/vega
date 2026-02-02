#PY511 
The third of five [[QM Axioms]].
## Composite Systems
Given
> $\ket{A}\in V,\ket{A}=\sum_na_n\ket{\psi_n}$ with basis states $\{\ket{\psi_n}\}$
> $\ket{B}\in V,\ket{B}=\sum_mb_m\ket{\phi_m}$ with basis states $\{\ket{\phi_n}\}$

The physical system of a composite system featuring two different Hilbert spaces $\ket{A}\in V,\ket{B}\in W$ can be completely described by a ray in the tensor product space $V\otimes W$.
> $\ket{A}\otimes\ket{B}=\sum_n\sum_ma_nb_m\ket{\psi_n}\otimes\ket{\phi_m}$

For a hydrogen atom, you can separate labels, to simplify some operators:
> $\ket{n,l,m_l;m_s}=\ket{n,l,m_l}\otimes\ket{m_s}$
> $L_3\ket{n,l,m_l;m_s}=L_3\ket{n,l,m_l}\otimes\ket{m_s}$
> $S_3\ket{n,l,m_l;m_s}=\ket{n,l,m_l}\otimes S_3\ket{m_s}$

States (most) can become entangled:
> If not, you can write $\ket{\Psi_{AB}}=\ket{\psi_A}\otimes\ket{\phi_B}$

The dimensions of this tensor product multiply such that:
> $\dim(V\otimes W)=\dim V\times\dim W$

Einstein's second greatest discovery:
> $\ket{\Psi_{AB}}=\frac1{\sqrt2}(\ket{0_A}\otimes\ket{0_B}-\ket{1_A}\otimes\ket{1_B})$

Alice could be in one place while Bob is somewhere else. We can prove that it's entangled by assuming that it isn't;
> $\ket{\Psi_{AB}}=\ket{\Psi_A}\otimes\ket{\Psi_B}$
> $=\alpha_0\beta_0\ket{0_A}\otimes\ket{0_B}+\alpha_1\beta_0\ket{1_A}\otimes\ket{0B}+\alpha_0\beta_1\ket{0_A}\otimes\ket{1_B}+\alpha_1\beta_1\ket{1_A}\otimes\ket{1_B}$
> $\to\alpha_0\beta_0=\frac1{\sqrt2}$
> $\to\alpha_1\beta_0=0$
> $\to\alpha_0\beta_1=0$
> $\to\alpha_1\beta_1=-\frac1{\sqrt2}$
> The system cannot be true.

We can still make an entire set of basis states that are each individually entangled.
> 10+01, 10-01, 00+11, 00-11;

Imagine Alice wants to send a qubit:
> $\ket{\phi_i}=\alpha\ket{0_i}+\beta\ket{1_i}$

How do you teleport the state without measuring it? The state can be "destroyed." Why can't you copy it?
> $\hat U_{cpy}(\ket{\phi_A}\otimes\ket{0_B})=\ket{\phi_A}\otimes\ket{\phi_B}$

The left-hand side is:
> $\hat U(\alpha_0\ket{0_A}\otimes\ket{0_B}+\alpha_1\ket{1_A}\otimes\ket{0_B})$
> $\alpha_0\ket{0_A}\otimes\ket{0_B}+\alpha_1\ket{1_A}\otimes\ket{1_B}$ (definition of copy)

The right-hand side is:
> $=\alpha_0^2\ket{0_A}\otimes\ket{0_B}+\alpha_1\alpha_0\ket{1_A}\otimes\ket{0B}+\alpha_0\alpha_1\ket{0_A}\otimes\ket{1_B}+\alpha_1^2\ket{1_A}\otimes\ket{1_B}$

As a result the system cannot be solved, making cloning impossible. However, teleportation might be a little more doable.
> $\ket{\phi_i}=\alpha\ket{0_i}+\beta\ket{1_i}$
> $\ket{\phi_f}=\alpha\ket{0_f}+\beta\ket{1_f}$
> $\ket{\Psi_{AB}}=\frac1{\sqrt2}[\ket{0_A0_B}+\ket{1_A1_B}]$

First entangle Alice's qubit:
> $\ket{\phi_i}\otimes\ket{\Psi_{AB}}=\frac\alpha{\sqrt2}\ket{0_i0_A0_B}+\frac\alpha{\sqrt2}\ket{0_i1_A1_B}+\frac\beta{\sqrt2}\ket{1_i0_A0_B}+\frac\beta{\sqrt2}\ket{1_i1_A1_B}$

The CNOT gate flips when the control qubit is $\ket1$ (an XOR). Applying it here:
> $U_{CNOT}\ket{\phi_i\Psi_{AB}}=\frac\alpha{\sqrt2}\ket{0_i0_A0_B}+\frac\alpha{\sqrt2}\ket{0_i1_A1_B}+\frac\beta{\sqrt2}\ket{1_i1_A0_B}+\frac\beta{\sqrt2}\ket{1_i0_A1_B}$

Meanwhile the Hadamard gate puts a known state into superposition. Applying it:
>$\hat U\ket{\phi_i\Psi_{AB}}=\frac\alpha{\sqrt2}\ket{+_i0_A0_B}+\frac\alpha{\sqrt2}\ket{+_i1_A1_B}+\frac\beta{\sqrt2}\ket{-_i1_A0_B}+\frac\beta{\sqrt2}\ket{-_i0_A1_B}$
> $=\frac12\ket{0_i0_A}\otimes[\alpha\ket{0_B}+\beta\ket{1_B}]$
> $+\frac12\ket{0_i1_A}\otimes[\beta\ket{0_B}+\alpha\ket{1_B}]$ (do an X gate)
> $+\frac12\ket{1_i0_A}\otimes[\alpha\ket{0_B}-\beta\ket{1_B}]$ (do a Z gate)
> $+\frac12\ket{1_i1_A}\otimes[-\beta\ket{0_B}+\alpha\ket{1_B}]$ (do a Y gate)

