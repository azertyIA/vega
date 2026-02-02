## 1. Signals
Most of the time analysis is done with the following formula, any source can be described witnh the following forms.
$$v(t)=Ri(t)$$
Signals are also a superposition of a bunch of fundamental frequencies, and amplifiers impact the amplitude, usually very linearly:
$$v_o(t)=A_vv_i(t)$$ $$v_oi_o=A_pv_ii_i:i_o=A_ii_i:A_p=A_vA_i$$
![[Pasted image 20251213223004.png]]
In general the typical amplifier equations given an input resistance and output resistance is as follows:
$$\frac{v_o}{v_s}=A_{vo}\frac{R_i}{R_s+R_i}\frac{R_o}{R_L+R_o}$$
There are four types of amplifiers: voltage, current, transconductance, and transresistance. Most of the time we just end up using transconductance amplifiers though. This one has both resistors ideal at infinity. So really it's an ideal output resistance of zero and an input resistance of infinity.

### 1.5. Input and Output Resistance
To determine input resistance, put an input voltage before the amplifier and see the current you get. To determine output resistance, turn off the input and measure the resistance from the output end.

### 1.6. High and Low Pass
A high pass network is given by a source connected to a capacitor splitting into the load and a grounded resistor. A low pass network is given by a source connected to a resistor splitting into the load and a grounded capacitor.
![[Pasted image 20251213230315.png]]
Analysis (keep in mind that when $\omega=\omega_0$, the decibels is -3):
$$A_{vL}=\frac{1/sC}{R+1/sC}=1/(1+sRC)=1/(1+j\omega/\omega_0)$$
$$20\log|A_{vL}|=-10\log[1+(\omega/\omega_0)^2]$$
$$A_{vH}=\frac{R}{R+1/sC}=1/(1+1/sRC)=1/(1-j\omega_0/\omega)$$
$$20\log|A_{vH}|=-10\log[1+(\omega_0/\omega)^2]$$
## 3. Semiconductors
In the silicon lattice, there can be holes and free electrons that disturb the natural order of the covalent bonds that the lattice makes. As free electrons act to fill in the holes, the process of recombination occurs. But as temperature increases, more of these electrons and holes exist.

## 3.1. Recombination
In thermal equilibrium, we can expect there to be as many holes as free electrons. The i in $n_i$ denotes intrinsic silicon.
$$n=p=n_{i}=BT^{3/2}\exp[-E_g/2kT]$$
$$np=n_i^2$$
Two different types of doping exist to disturb the lattice: pentavalent (donors, n-type) and trivalent (acceptors, p-type) impurities. Usually these will exist in higher concentrations than the free electrons due to temperature by default.
$$n_n=N_D:p_nn_n=n_i^2$$
$$p_p=N_A:p_pn_p=n_i^2$$
### 3.2. Drift
When an electric field is applied to a semiconductor crystal, holes are accelerated along the field and electrons are accelerated against the field. The resulting particles acquire a velocity characterized by hole mobility in units cm2/V-s:
$$v_{p-drift}=\mu_pE$$
$$v_{n-drift}=-\mu_nE$$
Now, given the concentration of a particle, the charge magnitude and the velocity, you can get charge density:
$$J_p=qpv_p=qp\mu_pE$$
$$J_n=-qnv_n=qn\mu_nE$$
$$\boxed{J=q(p\mu_p+n\mu_n)E=E/\rho=\sigma E}$$
This resistivity has units of Ohm-cm because it scales based on length/area. In fact multiplying everything by good enough units gets us a familiar Ohm's law.
$$(JA)=(EL)/(\rho L/A)=(\sigma A/L)(EL)$$
$$I=V/R=GV$$
### 3.3. Diffusion
When the density of charge carriers is not uniform, there is a tendency for the charges to want to balance out. This just uses a basic equation with some diffusion constants, $D_p$ and $D_n$. In intrinsic silicon, the diffusion of the electrons are much higher than the holes.
$$J_p=-qD_p\partial_xp(x)$$
$$J_n=qD_n\partial_xn(x)$$
$$D_n/\mu_n=D_p/\mu_p=V_t=kT/q$$
At room temperature, the final relation is often equal to $26$ mV.
### 3.4. PN Junction
When you put an acceptor block next to a donor block, some electrons will immediately try filling the holes from the donor to the acceptor and recombine to thermal equilibrium. From here it will be stated verbatim.

The holes that diffuse across into the n-region recombine with their duals and disappear. This also applies to the electrons from the n-region. When this instant recombination has been satisfied, there will be an amount of alien charges near the junction on both sides that failed to recombine. 

These alien charges create a depletion region, generating an E-field between the two blocks. This E-field pushes holes back towards the p-region and electrons towards the n-region, thereby opposing the diffusion of charged particles. As this field exists over a distance known as the depletion region there is a voltage drop across the two blocks that limits the overall current of the charged particles, but keep in mind that:
$$I_s=A\sigma E=V_0/R$$
So this current caused by the depletion voltage (0.6 - 0.9) can be attributed to an equal and opposite drift current in equilibrium:
$$I_D=I_S=V_0/R=(V_T/R)\ln(N_AN_D/n_i^2)$$
If the blocks were inequal or such a case where $N_A\neq N_D$, the charge dissipation across the depletion lager should be the same, though the widths may not be the same.
$$\boxed{|Q|=AqN_Ax_p=AqN_Dx_n}$$
As a result the ratio of widths can be found and thus the total width of the depletion layer can be found:
$$x_n/x_p=N_A/N_D$$
$$W=x_n+x_n=\sqrt{\frac{2\epsilon_s}q(\frac1{N_A}+\frac1{N_D})V_0}$$
$$x_n=N_A/{N_A+N_D}$$
$$x_n=N_D/{N_A+N_D}$$
### 3.5. PN Applied Voltage
It's a lot easier to think that the voltage of $V_0$ is going to be much bigger than the forward bias should be. As a result the voltage drop should across the region should take into effect the external voltage source. In reverse bias, the two voltages should add in magnitude, in forward, the opposite.

In the reverse bias case, the voltage drop grows greater, meaning that the resulting diffusion goes to zero. Meanwhile the drift is all that's left.

In the forward bias case, means current will pass :).


## Diode Circuits
There is a depletion region that gets bigger in reverse bias and smaller in forward bias (p to n). The I-V characteristic is exponential.

There are a few models to represent this exponential:
- Ideal Diode: delta function at V = 0V (wire)
- Voltage Drop:  delta function at V = 0.7V (battery)
- Small Signal: linear approximation at bias point (id = Id/Vt) (resistor)
- Zener Reverse: linear breakdown at some negative voltage (battery and resistor)

Some circuits that we looked at are
- rectifiers
- power supplies
- clamping circuits
![[Pasted image 20251214175830.png]]
An example of a voltage clamper. When the voltage is too much or too little, the diodes turn on and set the voltage for real across the resistor. Just treat all of them as short circuits until current flows the wrong way.
$$i=I_S(e^{v/V_T}-1)$$
## Transistors

## 5. MOSFETS

The MOSFET has an electric field controlled current, so no current at the gate. For example, the NMOS transistor has an oxide in between the gate and the body, helps generates an inversion channel (Vgs) in the body which allows drift current to occur, controlled by Vds. (Cox is measured in F/m2)
$$\mu_n(\frac\epsilon t)(\frac WL)=\mu_nC_{ox}\frac WL=K$$
The overall drift current is given by:
$$I=Q/L*v=(CWv_{OV})(\mu_nv_{DS}/L)=Kv_{OV}v_{DS}=g_{DS}v_{DS}$$
When $v_{DS}$ grows to be more significant, then a tapered channel forms:
![[Pasted image 20251214194921.png]]
As a result, the effective voltage becomes the average of the two endpoints: $(v_{OV}-\frac12v_{DS})$.
$$I=K(v_{OV}v_{DS}-\frac12v^2_{DS})$$
When $v_{DS}$ grows bigger than the overdrive voltage, then the channel gets fully pinched and no amount of drain-source voltage changes anything. The effective voltage is now just $\frac12v_{OV}$.
$$I=\frac12Kv^2_{OV}$$
In general:
$$I_{DS}|_{Vds<Vov}=K(V_{GS}-V_t)V_{DS}-\frac12V_{DS}$$
$$I_{DS}|_{Vds>Vov}=\frac12V_{OV}^2$$
The MOSFETs have an inherent saturation resistance determined by the early voltage.
$$r_0=V_A/I_D=1/\lambda I_D$$
At a fixed DC point to when the MOSFET is active, small variations in voltage will see an approximately linear relationship to current.
$$\delta I_D=\frac12K(2V_{OV}\delta V_{OV})=(KV_{OV})\delta V_{OV}$$
There are two models for the MOSFET, the TT (pi) and T (t) models. In general if the source is grounded, use the TT model, otherwise use the T model.
$$r_\pi=\infty$$
$$r_s=1/g_m$$
$$r_0=V_A/I_D$$
$$g_m=KV_{OV}$$

For most amplifiers, find the DC bias point and use that to parameterize the AC small signal circuit.
#### Common Source (CS)
![[Pasted image 20251215053456.png]]
Better solved with the pi model.
$$A_{v0}=-g_m(r_0||R_D)$$
$$R_o=(r_0||R_D)$$
#### Common Gate (CG)
![[Pasted image 20251215053506.png]]
Better solved with the pi model.
$$A_{v0}=(1+g_mr_o)(R_D/R_D+r_o)$$
$$R_o=(r_0||R_D)$$
#### Common Drain (CD)
![[Pasted image 20251215053523.png]]
$$A_{v0}=(1||g_mR_S)$$
$$R_o=(1/g_m||R_S)$$

## 6. Bipolar Junction Transistor

The BJT should be more seen as two diodes that are facing into each other (pnp) or away from each other (npn). The current coming from the base pin is distributed among the two diodes.

There are a few situations for each type of activity in the diodes:
- BE on, CE off: active
- BE on, CE on: saturation
- BE off, CE off: off

In the active made of this, relations can be made about the currents coming from these pins:
$$I_C=I_Se^{V_{BE}/V_t}$$
$$I_B=I_C/\beta,I_E=I_C/\alpha=I_B+I_C$$
In saturation mode, the beta factor of the transistor will be noticeably less than the active beta. The edge of saturation is as such:
$$V_{BC}=0.4V,V_{CE}=0.3V$$
For the transconductance derivation:
$$\delta{I_C}=I_Se^{V_{BE}/V_t}(\delta V_{BE}/V_t)=(I_C/V_t)\delta V_{BE}$$
For the pi and t models:
$$r_0=V_A/I_C$$
$$r_\pi=V_{BE}/I_B=\beta/g_m$$
$$g_m=I_C/V_t$$
$$r_e=\alpha/g_m$$
#### Common Emitter (CE)
![[Pasted image 20251215053542.png]]
Better solved with the pi model.
$$A_{v0}=-g_m(r_0||R_D)$$
#### Common Base (CB)
![[Pasted image 20251215053552.png]]
$$A_{v0}=(1+g_m)(r_0||R_D)$$
#### Common Collector (CC)
![[Pasted image 20251215053617.png]]
$$A_{v0}\approx R_E/(r_e+R_E)\approx(1||g_mR_E)$$
## Integrated Circuits

### Current Steering

To transfer current across a dense chip, transistors can be used as current sources by connecting gates to other gates, as $V_{GS}$ is the only thing that matters in determining current. This thereby mirrors the current somewhere else. We have a say in the scaling of this mirrored current by changing the transistor geometry. 

It also is going to be difficult to incorporate amplifiers because coupling capacitors are difficult to insert in such circuits. Putting a PMOS (fixed current) in series with a gate-controlled NMOS, gives you an output at the drain:
$$I_P=\frac12KV_{OV}^2=\frac12K(V_{DD}-V_G-V_t)^2$$
$$g_m=KV_{OV}=\sqrt{2I/K}$$
### Cascode Amplifiers

This amplifier takes a current at the start of the drain and puts it in series with another gate-controlled NMOS. Then take the drain voltage of the first as a function of the gate voltage of the second.

### Differential Amplifier

Two voltages are sampled in DC and the output at the drains is a function of the difference. The current is set at the sources splitting across the two voltages. 

### Frequency Dependence

On the exam all that matters is high frequency response. The poles are at -3dB. The effective time constant can be calculated with RC. For instance the MOSFET has the following capacitances:
- gate-source
- gate-drain converted to equivalent gate-source capacitor

These capacitances can be added and multiplied by signal resistance to get a time constant.

For the common-emitter:
- base-emitter
- base-collector converted to equivalent base-emitter capacitor

$$C_{eq}=C_\mu(1+g_mR_L)\to\tau=C_{in}(r_{sig}||r_\pi)$$
### Open Circuit Time Constants

You can approximate
$$\omega=\Sigma1/\tau$$
