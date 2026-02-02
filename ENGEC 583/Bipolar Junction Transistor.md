![[Pasted image 20260129150829.png]]
The BJT comes with three different nodes: the base (B) the emitter (E) and the collector. From the side, it looks like an onion. From the top, it also looks like an onion. 

To turn this into an active component, define an input port and an output port. The input voltage goes across $V_{BE}$ and the output voltage goes across $V_{CE}$. Then you have to say the I-V characteristics of the input and output ports.

However, the BE junction literally is a PN diode, which is modeled with the simplest functions in existence. CE also a diode (in a way). So it's either on, or off. 
![[Pasted image 20260129151234.png]]
$i_b$ controls the I-V characteristic of the CE port. But there are notable places where things matter. For example saturation occurs beyond the changing part. Cutoff happens if $i_b$ is not big enough. Everything else is active.