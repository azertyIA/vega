![[Pasted image 20260129150829.png]]
The BJT comes with three different nodes: the base (B) the emitter (E) and the collector. From the side, it looks like an onion. From the top, it also looks like an onion. The conductors are also rings to connect to the ports.

To turn this into an active component, define ***an input port and an output port***. A **single port** features **two terminals** (because one voltage doesn't make sense). 

The input voltage goes across $V_{BE}$ and the output voltage goes across $V_{CE}$. Then you have to say the I-V characteristics of the input and output ports.

However, the BE junction literally is a PN diode, which is modeled with the simplest functions in existence. CE also a diode (in a way). So it's either on, or off. 
![[Pasted image 20260129151234.png]]
$i_b$ controls the I-V characteristic of the CE port. But there are notable places where things matter. For example saturation occurs beyond the changing part (edge of saturation $V_{sat}=0.4$ but basically nothing compared to cutoff voltage). Cutoff happens if $i_b$ or $V_{BE}$ is not big enough. Everything else is active.

![[Pasted image 20260203145124.png]]
There are two biases featured in an active BJT: a forward-bias PN junction across BE and reverse-bias PN junction across CB. Holes don't move as easily as the freely moving electrons because they definitionally cannot escape the lattice!

### Aside: Plasma Technologies and Microchip Technologies
So why does current still flow despite the diode being in reverse bias? It's because the voltage of the applied voltage overwhelms the built-in electric field. Especially if it's a big electric field. A diode is a reservoir of electrons, but there are only so many. What does this mean???

### BJT as a Current Controlled Current Source
The proportionality constant that matters is the $\beta$ value which denotes the collector-base current ratio. As such, the BJT can be seen as a current amplifier. As an off-note, the transformer generates a higher voltage given more turns on the secondary, but less current. So how can you make a photo-diode by adding a lens from the sunlight?

### BJT as a Logic Gate
![[Pasted image 20260205142858.png]]
There are three modes of operation for the BJT, cutoff, active and saturation. 
- the BJT is in the **cutoff** region ($V_I$ before the turn-on voltage $v_f$) then $V_O$ will not be pulled down to ground. 
- the input voltage is too high ($V_{I.sat}$), then your output will be **saturated** ($v_{sat}$) or at around 0.3V. 
- otherwise the characteristic will be just about linear (through $R_C$) in the **active** mode.

To find the linear characteristic, $i_B$ can be found by seeing the voltage drop across $V_I$ and $v_f$ and dividing by the $R_B$ resistor. Then your new function will become:
$$V_O=V_{CC}-A(V_I-v_f)=-AV_I+[V_{CC}+Av_f]$$
$$A=\beta R_C/R_B$$
To find the input saturation voltage, set $V_O=V_{sat}$:
$$V_{I.sat}=(V_{CC}-V_{sat})/A+v_f$$
To make this ideally digital, increase the slope by a FUCKTON. Raise $R_C/R_B$ because that's all you can control. 