Quiz next Monday: Diodes and MOSFETs. 

The exam sits on October 6: 
- circuits
- diodes
- DC properties of MOSFETS and BJTs.

## MOSFETs

There are two different flavors of MOSFETS: NMOS and PMOS:
- NMOS usually have electrons move from source to drain. (NPN)
- PMOS usually have holes move from source to drain. (PNP)

When the gate voltage is greater than zero in the NMOS, electrons get pulled towards the gate near the oxide, allowing for a channel to build. When enough electrons have built at the surface from enough voltage ($v_t$), the p-type inverts to an n-type and conduction can occur. When the drain is greater than zero, electrons can be conducted from the source to the drain (current from drain to source).

When the gate voltage is less than zero in the PMOS, holes are pulled towards the gate, allowing for a hole channel to build. When the voltage passes a threshold, the n-type base creates a p-type region and allows conduction. When the drain voltage is less than zero, holes can be conducted from the source to the drain (current from source to drain).

Three regimes occur:
- $|V_g|<|V_t|$, no connection no matter what
- $|V_g|>|V_t|$: $V_{DS}$ small, almost like a small resistor
- $|V_g|>|V_t|$: $V_{DS}$ big ($\geq V_{GS}-V_t$), curve flattens out

For the resistor phase:
> $I_{DS}=\frac WL\mu_nC_{ox}(V_{GS}-V_t)V_{DS}$
> $W$, $L$: width and length of the channel
> $\mu_n$: electron mobility in the channel
> $C_{ox}$: oxide capacitance per area = $\epsilon/t$ (thickness)

When $V_{DS}$ gets bigger, the linear relationship disappears and the curve saturates:
> $I_{DS}=\frac WL\mu_nC_{ox}[(V_{GS}-V_t)V_{DS}-\frac12V_{DS}^2]$

Saturation is caused by an uneven channel until the drain side just has no channel connected to it. The channel is effectively pinched off.

In the other case, it acts like a diode where the current is exponential to $V_{GS}-V_t$
> $k_n=\mu_nC_{ox}$ (NMOS)
> $k_p=\mu_pC_{ox}$ (PMOS)
> $V_{0V}=V_{GS}-V{t}$
> $I_D^{sat}=\frac WL\frac k2V_{0V}^2$

Given:
> $\frac WL=10$
> $t_{ox}=8$ nm
> $\epsilon_{ox}=3.9\epsilon_0$
> $\mu_n=450$ cm2/Vs
> $V_t=0.7$ V
> $I_{DS}=100$ uA

So,
> $C_{ox}=\epsilon_{ox}/t_{ox}=4.3\times10^{-7}$ C/V/cm2
> $k=\mu_nC_{ox}=1.9\times10^{-4}$ A/V2
> $I_D^{sat}=(10)(1.9\times10^{-4})(V_{GS}-0.7)^2/2=100\times10^{-6}$

Solve for V.

The resistance isn't completely linear. For example, channel length modulation exists by adding a term to the saturation current that is added by some $\lambda V_{DS}$ (dependent on manufacturer constants).

The body effect occur when the source and body are not connected, so the threshold voltage increases:
 > $V_t=V_{t0}+\gamma(\sqrt{2\phi_F+V_{SB}}-\sqrt{\phi_F})^2$
 > $V_{SB}$: voltage difference between source and body
 > $\phi_F$: some random ass voltage
 
 A CMOS sits each MOSFET next to each other. There are a few ways of drawing it out. But the arrow matters and the body is probably connected to ground.

Let's try anything:
> $I_D^{sat}=(10)\frac{400\times10^-6}2(V_GS-0.5)^2=180\times10^{-6}$
> $2(V_GS-0.5)^2=0.18$
> $(V_GS-0.5)^2=0.09$
> $V_{GS}=0.8$ V

> $V_{GS}=0.8=0-V_S$
> $V_S=-0.8$ V

Saturation occurs when:
> $V_{DS}\geq V_{GS}-V_t$

Here we go:
> $I_D=(1)\frac{20*10^{-3}}{2}(V_{GS}-0.5)^2=0.9*10^{-3}$
> $10(V_{GS}-0.5)^2=0.9$
> $V_{GS}-0.5=0.3$

$V_{GS}=0.8$

$V_{DS}\geq 0.8-0.5$

