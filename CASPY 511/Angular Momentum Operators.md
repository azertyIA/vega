The Jacobi Identity generates a Lie Algebra:
$$[\hat J_i,\hat J_j]=i\hbar\epsilon_{ijk}\hat J_k$$
The generator of rotations about a unit normal $\hat n$ is:
$$R(\theta)=e^{-i\hat J\cdot\hat n\theta/\hbar}$$
This has a rotational symmetry which creates a non-commuting group characterized by the underlying Lie Algebra. Such can be extended to spin which cannot be expressed as something simple as a cross-product. Spin also requires a 720 degree rotation to return the spin-half system to its initial state.
$$\vec L=\vec r\times\vec p=m\vec r\times\vec v$$
$$\vec S=e^{-i\hat S\cdot\hat n\theta/2\hbar}$$

So is $\hat J=\hat L+\hat S$ an angular momentum?
$$[J_i,J_j]=[L_i+S_i,L_j+S_j]$$
$$=[L_i,L_j]+0+0+[S_i,S_j]$$
$$=i\hbar\epsilon(L_k+0+0+S_k)$$
$$=i\hbar\epsilon J_k$$
What about $\hat K=\hat L-\hat S$?
$$[K_i,K_j]=[L_i-S_i,L_j-S_j]$$
$$=[L_i,L_j]+0+0+[S_i,S_j]$$
$$=i\hbar\epsilon(L_k+0+0+S_k)$$
$$\neq i\hbar\epsilon K_k$$
So what the fuck?

## Formal Theory of Angular-Momentum Addition

Base kets in the $\hat J$ Hilbert space can be written with the following commutator. 
$$[J^2,J_z]=[J_x^2+J_y^2+J_z^2,J_z]$$
$$=J_x[J_x,J_z]+[J_x,J_z]J_x+J_y[J_y,J_z]+[J_y,J_z]J_y$$
$$=J_x(i\hbar\epsilon)J_z+[J_x,J_z]J_x+J_y[J_y,J_z]+[J_y,J_z]J_y$$
Or, it can give the ket $\ket{j,m}$, and more than one can be (un)coupled together into a basis
$$\ket{j_1,m_1}\otimes\ket{j_2,m_2}=\ket{j_1,j_2,m_1,m_2}$$
It can be coupled together as such:
$$J_z=J_{1z}+J_{2z}$$
$$[J^2,J_{1z}]=0$$
$$[J^2,J_{2z}]=0$$
And can be written in a linear combination as such:
$$\ket{j_1,j_2;j,m}=\Sigma_{m1}\Sigma_{m2}\braket{j_1,j_2;m_1,m_2|j_1,j_2;j,m}\ket{j_1,j_2;m_1,m_2}$$
$$=\Sigma_{m1}\Sigma_{m2}C(j_1,m_1,j_2,m_2,j,m)\ket{j_1,j_2;m_1,m_2}$$
Cool things about these coefficients they vanish unless a certain condition is met:
$$(J_z-J_{1z}-J_{2z})\ket{j_1,j_2;j,m}=0$$
$$(m-m_1-m_2)\braket{j_1,j_2;m_1,m_2|j_1,j_2;j,m}=0$$
$$(m-m_1-m_2)C(j_1,m_1,j_2,m_2,j,m)=0$$
$$\boxed{m=m_1+m_2,C\neq0}$$
## Wigner-Eckhart Theorem

Where $q=-k,-1,0,1, k$;
$$\braket{j',m'|T_q^{(k)}|j,m}=\braket{j,m;k,q|j,m}F_{j'j}^k$$
The dipole moment operator is written as the following:
$$\vec d=-e\vec r=\braket{(x+iy)/\sqrt2,(x-iy)/\sqrt2,z}$$
The dipole symmetry selection rules state that:
$$\Delta l=\pm1,\Delta m_l=0,\pm1$$