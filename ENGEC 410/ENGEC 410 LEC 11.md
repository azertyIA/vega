In the BJT however, we have the following relations:
> $V_{CE}=V_{CC}-i_CR_C$
> $=V_{CC}-I_SR_C\exp V_{BE}/V_T$

Given another small signal in V_GS through an oxide:
> $V_{GS}=V_{GS0}+v_{gs}(t)$
> $I_D=\frac12 k(V_{GS}-V_T)^2$
> $=\frac12 k(V_{GS0}+v_{gs}(t)-V_T)^2$
> $=\frac12 k(V_{OV}^2+2v_{gs}(t)V_{OV})$
> $=\frac12 kV_{OV}^2+kv_{gs}(t)V_{OV}$
> $=I_{D0}+i_D(t)$

Transconductance is the $g_m=-kV_{OV}$ coefficient to the small signal in the current.
> $V_{DS}=V_{DD}-I_DR_D$
> $=V_{DD}-I_{D0}R_D-i_D(t)R_D$
> $=V_{DD}-V_{DS0}-i_D(t)R_D$
> $=V_{DS0}-kR_DV_{OV}$
> $=V_{DS0}+v_{ds}(t)$

So the equivalent circuit looks like a dependent current source.
> $i_D(t)=kV_{OV}*v_{gs}(t)$

There is a resistance $r_0$ across from the current source with value $V_A/I_D$. Now time for some examples.
```
// scratch work
k=2.4 mA/V2
Vt = 1V
VA = 15 V
VGS = 1.5V

// part A: Vov = 0.5 V
Id = 1.2(0.25)=0.3 mA
r0 = 15/0.3 = 50 kO
gm = -1.2 mA / V

// part B: Id = 0.5 mA
.5 / 1.2 = 0.41, Vov = 0.64 V
r0 = 15/0.5 = 30 kO
gm = 0.64 * 2.4 = -1.53 mA / V
```

BJTs work a bit differently.
> $I_C=I_S\exp V_{BE}/V_T$
> $I_E=I_C/\alpha$
> $I_B=I_C/\beta$

So, the small signal form would look like:
> $V_{BE}=V_{BE0}+v_{be}(t)$
> $I_C=I_S\exp(V_{BE0}+v_{be}(t))/V_T$
> $=I_S(\exp V_{BE0}/V_T)(\exp v_{be}(t)/V_T)$
> $=I_S(\exp V_{BE0}/V_T)(1+v_{be}(t)/V_T)$
> $=I_S\exp V_{BE0}/V_T+(I_S\exp V_{BE0}/V_T)v_{be}(t)/V_T$
> $=I_{C0}+(I_S\exp V_{BE0}/V_T)v_{be}(t)/V_T$
> $=I_{C0}+I_{C0}v_{be}(t)/V_T$
> $=I_{C0}+i_c(t)$

So the transconductance is:
> $g_m=I_{C0}/V_T$

And through the base:
> $I_B=I_C/\beta$
> $=I_C/\beta+i_c(t)/\beta$
> $=I_{B0}+i_b(t)$

As equivalent circuits, there is a resistor between B and E (with v0) and E and C. There is also a current source with current $g_mv_0$. There is a T-model where there is a T junction with a current source ($\alpha v_0$) on the C side and a resistor (with v0) on the E side.

```
// scratch
Veb = 0.7
Ve = 0.7, Ie = .93 mA
Ic = .92 mA
Vc = -5.35 V

alpha = .991
ie = - vi / re
vo = ie * re 
```