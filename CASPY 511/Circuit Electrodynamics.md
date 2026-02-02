Given a simple LC circuit, it's basically a harmonic oscillator:
$$Q=Cv=-C\partial_t\Phi$$
$$\Phi=L\partial_t Q=LC$$
$$\ddot\Phi+\frac1{LC}\Phi=0\to\omega=\frac1{\sqrt{LC}}$$
Uhh, so there's a fourth thing called the Josephson Junction (JJ):
$$I=I_0\sin(2\pi\frac{Vt}{h/2e})=I_0\sin(2\pi\frac\Phi{\Phi_0})$$
![[Pasted image 20251118145403.png]]
To quantize this we can set general coordinates for $x,\dot x$ to be $\Phi,\dot\Phi$ or $Q,\dot Q$ and get a [[Lagrangian Mechanics|Lagrangian]].
$$T=\frac12C\dot\Phi^2$$
$$V=\frac1{2L}\Phi^2$$
$$L=T-V=\frac12(C\dot\Phi^2-\frac1L\Phi^2)$$
And now we can translate it into [[Hamiltonian Mechanics]]:
$$p=\partial_\dot\Phi L=C\dot\Phi=Q$$
$$H=\dot\Phi Q-L$$
$$=\dot\Phi Q-\frac12(C\dot\Phi^2-\frac1L\Phi^2)$$
$$=\frac1CQ^2-\frac12(\frac1CQ^2-\frac1L\Phi^2)$$
$$=\frac1{2C}Q^2+\frac1{2L}\Phi^2$$
This entire thing correlates to:
$$\hat H=\hbar\omega(\hat a^\dagger\hat a+\frac12)$$
$$\Delta_\Phi=\sqrt{\hbar/2C\omega}=\sqrt{\hbar/2Z}$$
$$\Delta_Q=\sqrt{\hbar C\omega/2}=\sqrt{\hbar Z/2}$$
This is cool and all but this doesn't work for capturing a qubit.

You actually have an anharmonic oscillator when using a JJ. Because it's not exactly a harmonic oscillator, you can create a two level system with the known energies of the bottom two levels. The levels above the first two get narrower and narrower.

$$M\vec x=\lambda x$$
$$(M-\lambda I)\vec x=\vec 0$$