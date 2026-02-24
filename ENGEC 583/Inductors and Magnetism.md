![[Pasted image 20260219135947.png]]
Imagine a toroidal inductor. It has some amount of turns, so the resultant magnetic field would be:
$$\oint d\vec l\cdot\vec H=2\pi r_0H_\phi=Ni(t)$$
$$H_\phi=Ni(t)/2\pi r_0=Ni(t)/l$$
But Faraday's says another thing:
$$V_{ind}=-AN\partial_t\vec B=-\mu AN\partial_tH_\phi$$
Combining the two gets you the inductance law.
$$V_{ind}=-(\mu AN^2/l)*\partial_ti$$

When something is linear you can always almost be able to apply superposition. In differential equations, you can superimpose some solutions because your system is linear. In a linear transformer, there are two linear inductors, each with their own i-v characteristics:
$$V_1=L_1\partial_tI_1\pm M\partial_tI_2$$
$$V_2=L_2\partial_tI_2\pm M\partial_tI_1$$
For an ideal inductor which is a linear inductor that is coupled perfectly and prevents power loss, you lose current where you gain voltage.  
$$V_1/V_2=N_1/N_2=-I_2/I_1$$
