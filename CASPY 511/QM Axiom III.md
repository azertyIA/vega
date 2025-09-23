#PY511 
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
