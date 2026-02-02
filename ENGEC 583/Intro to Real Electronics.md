Let's hope I can fill in the background information, but allegedly a lot of the stuff I'm learning comes straight from Lee's research.

### The Atoms of Electronics
A decibel is NOT a unit. It's a scale related to the logarithm of gain. You can accommodate several orders of magnitude of values compared to the linear scale. Phasor form is used to do easier math basically. It's used to model sines and cosines without having to deal with sines and cosines. 
$$A\cos\omega t\mapsto Ae^{i\omega t}$$
To solve differential equations you end up with two different terms: the particular solution and the homogeneous solution.
$$\hat A(x_h+x_p)=Ax_h+0$$
### Circuits
The simplest of the circuits out there is the RC circuit. This can be modeled with the following equation:
$$V_C=V_S-RI=V_S-RC\partial_tV_C$$
$$\partial_tV_C=-V_C/RC+V_S/RC$$
$$V_C(t)=V_N(t)+V_F(t)=Ae^{-t/RC}+BV_S(t)$$
> Usually in these circuits, quantities such as RC are related via $t<$ similar to how materials have a conductance metric.

Most power outlets have pure, monochromatic frequencies. DC is also technically monochromatic. 

### Faraday's Law
This is Faraday's Law in both calculus forms:
$$\nabla\times\vec E=-\partial_tB$$
$$\iint d\vec s\cdot(\nabla\times\vec E)=\oint d\vec l\cdot\vec E=-\partial_t\iint d\vec s\cdot\vec B=-\partial_t\Phi_B$$
### Scratch
$$\partial_tVe^{\omega t}=-Ve^{\omega t}/RC$$
$$\omega Ve^{\omega t}=-Ve^{\omega t}/RC$$
$$\omega=-1/RC$$
