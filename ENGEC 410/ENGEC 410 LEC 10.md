When talking about BJTs, there's basically two diodes back to back or front to front. 

The current given a junction is as follows:
> $i_C=I_S\exp(V_{BE}/V_t)$
> $i_B=i_C/\beta$
> $i_E=i_C/\alpha$

For pnp transistor, $V_{EB}$ applies. Let's take an example:
> $V_{BE}=0.7 V$, $V_E=3.3V$ 
> $i_C=I_S\exp(V_{BE}/V_t)$
> $i_E=i_B+i_C=3.3V/3.3k\Omega=1mA$
> $i_C=\alpha i_E=(100mA/101)$
> $i_B=1mA/101$
> $V_C=10V-4.7V/1.01=5.3V$

And another example:
> $V_{EB}=0.7V$
> $I_E=4.65mA$
> $I_C=4.65mA$
> $V_C=-5.35V$

We can use both BJTs and MOSFETs as amplifiers. In the case of MOSFETs:
> $i_D=\frac12kV_{OV}^2$, voltage controlled current ($V_{DS}>V_{OV}$)

If we have a high voltage behind a resistor connected to drain ($V_S=0$), with the resulting drain voltage being:
> $V_{DS}=V_D=V_{DD}-i_DR_D$
> $i_D=\frac12kV_{OV}^2$
> $V_{DS}=V_D=V_{DD}-\frac12kV_{OV}^2R_D$
> $=V_D=V_{DD}-\frac12k(V_{GS}-V_T)^2R_D$

And that's a function of $V_{GS}$ for $V_D$, which looks like a upside down offset parabola. This is valid for the region between the two following points:
> $V_{GS}=V_T$ (between no current and saturation)
> $V_{GS}=V_{DS}+V_T$ (between saturation and triode)
> $V_{GS}=V_{DD}$ (good luck)

The second point looks like:
> $V_{DS,B}=V_{DD}-\frac12k(V_{DS,B})^2R_D$, a quadratic equation which you can get a solution for
> $0=-V_{DD}+V_{DS,B}+\frac12kR_DV_{DS,B}^2$
> $V_{DS,B}=\frac1{kR_D}(\sqrt{2kR_DV_{DD}+1}-1)$
> $V_{GS,B}=V_T+\frac1{kR_D}(\sqrt{2kR_DV_{DD}+1}-1)$

The third point looks like:
> $V_{DS,C}=V_{DD}-kR_D(V_{GS}-V_t)V_{DS,C}$
> $V_{DS,C}=V_{DD}-kR_D(V_{DD}-V_t)V_{DS,C}$
> $V_{DS,C}+kR_D(V_{DD}-V_t)V_{DS,C}=V_{DD}$
> $(1+kR_D(V_{DD}-V_t))V_{DS,C}=V_{DD}$
> $V_{DS,C}=V_{DD}/(1+kR_D(V_{DD}-V_t))$

For a small signal, the gain is given by:
> $V_{GS}=V_{GS0}+v_{gs}(t)$
> $A=\partial_{GS}V_{DS}$
> $A=\partial_{GS}(V_{DD}-i_DR_D)$
> $=-\frac12kR_D\partial_{GS}(V_{GS}-V_T)^2$
> $=-kR_D(V_{GS}-V_T)$
> $A=-kR_DV_{OV}$

An example to have a gain of $-10$:
> $V_{OV}=0.2V$, $k=0.4mA/V^2$
> $R=125k\Omega$
> $i_D=0.008mA$
> $V_{DS}=0.8 V$
