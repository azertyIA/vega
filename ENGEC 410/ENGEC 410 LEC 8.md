👅👅👅

For the exam you get one thing of notes (front). Calculators definitely necessary.

Diodes
- fundamental device physics
- IV characteristics/models
- circuits with diodes

MOSFETs
- Fundamentals, modes of operation

BJTs
- Fundamentals, I-V, modes of operation

Drift-diffusion equations of junctions:
- Drift with an E-field:
	- $\vec J=\sigma\vec E=ne\mu\vec E$
- Diffusion with a density gradient:
	- $\vec J=e\nabla n(D_n)$

Diodes:
- There is a diffusion barrier between the p and n types. The resulting current is
- $I_D=I_S(e^{eV/k_BT}-1)$
- Some models include the one that you already know. (Ideal, Voltage Drop, Linear)

MOSFETs:
- Current flow when $V_{GS}>V_t$
	- $I_D=\frac WLk[V_{OV}-\frac12V_{DS}]V_{DS}$
- Saturation when $V_{DS}\geq V_{GS}-V_t$
	- $I_D=\frac WLk(\frac12V_{OV}^2)$
- PMOS be the same type shit.
- On when Vg, Vd, high and Vs low
- PMOS off when opposite

CMOS inverter:
- PMOS NMOS connected at drains (Vout), sources at Vdd for PMOS and ground for NMOS. Vin at gates.

BJTs, yippee!!!
- There are three nodes in a BJT. An N(++)P(+)N and P(++)N(+)P are transistors that run on diffusion current. In an NPN, the current goes into the base and collector while out of the emitter. Meanwhile, the PNP has current go into the emitter and out of the base and collector.
- $V_{BE}>0$: electrons diffuse from E to B to C.
- $V_{BC}<0$: the BC diode turns off.
- The thing only works now if both of these are true.
- The opposite is true for a PNP. The doping creates a difference in current between electrons and holes. Electrons move out of the EB through the C which has a current and the holes moves from B to E which has a current.
- $I_C=I_{EB}^e=I_Se^{eV/kT}$
- $I_B=I_{EB}^h=\frac{I_S}\beta e^{eV/kT}$ 
- $I_C>I_B$
- $I_E=I_B+I_C=\frac{I_C}\alpha$
- $\alpha=\frac\beta{\beta+1}\approx1$

Saturation occurs when $V_{CE}<0.3$, $V_{BC}>0.4$ or when both diodes are on. $V_{CE}$ low creates saturation this time, while big difference creates activity. Smaller creates a deeper saturation.

NPN has high $V_C$ and high $V_B$ and low $V_E$.