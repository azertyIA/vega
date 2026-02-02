Silicon is just about everywhere. In the earth, rocks and glass. But you need to make that pure in order to do cool semiconductor stuff. When you include an impurity into the silicon lattice, you can add a group V (electron) or a group III (hole). This will as a result, add conductivity to your material, making silicon a proper semi-conductor.

![[Pasted image 20260129135235.png]]
Putting these two semi-conductors together in a V-III (np) block, the extra electrons will move to the III block and the holes will move to the V block (via diffusion).

Initially though, everything is neutral (so there is as many electrons as protons), so when they start moving, they leave behind the opposite charge, inducing a built-in electric field. This built-in electric field results in a voltage drop across the diode. The true I-V nature of the diode is modeled with an exponential usually:
$$i_D=I_S[e^{V_D/\eta V_t}-1]$$
- the saturation current $I_S$ spans in the picoamp range
- the thermal voltage $V_t$ is related through thermodynamics $eV_t=k_BT$
- the emission coefficient $\eta$ is either $1$ or $2$.

It's weird to use an exponential, so usually we establish an operating point that our input values will sit around (establish a Taylor expansion). From here we approximate linearly:
$$i_D+\delta i_D=I_S[e^{(V_D+\delta V_D)/\eta V_t}-1]$$
$$\delta i_D\approx I_S[1-1+(V_D-V_D+\delta V_D)/\eta V_t]\approx I_S\delta V_D/\eta V_t$$
The PN Junction can also be represented linearly using a voltage source (spans $0.5$ to $0.8$ V) and a resistor. If we take a different route for approximation:
$$g=1/r=\partial_Vi_D=\frac{I_S}{\eta V_t}e^{V/\eta V_t}\approx i_D/\eta V_t$$
$$V_r=r_Di_D=\eta V_t=\eta k_BT/e$$
- $e$ is given by $1.602\times10^{-19}$ J
- $V_t$ is given by $25$ mV
- $k_B$ is given by $1.38\times10^{-23}$ J/K
- $T$ is given by $300$ K

You'll find that the voltage drop across the resistor is extremely small anyways, so most people just use the battery at $0.7$ V. So let's recap: exponential -> linear -> resistor too small -> infinite. Power is not generated in a passive element (aka the thing should not be amplified). 
### The Photodiode
If you shoot photons at the built-in electric field $\vec E$, then they will start shooting off electrons off their orbit, and will start moving towards the positive side of the electric field (in group V).