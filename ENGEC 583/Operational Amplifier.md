![[Pasted image 20260203135536.png]]
The operational amplifier has two nodes of operation: the linear regime, and the saturated regime. The linear regime stops when the amplified difference surpasses the supplied voltage:
- linear: $V_O=A(V_P-V_N)$ (the gain is ideally infinite)
- saturation: $V_O=\pm V_{CC}$

In an ideal operational amplifier the two input ports should be the same voltage, but somehow there is no current flowing between the two? How would that behave if there is no simple resistor in the middle? In other words, there is open circuit current ($r=\infty$) but short circuit voltage ($r=0$). So what's the resistor? Let's assume an infinite input resistor for now. 

An **operational amplifier** is the combination of many many transistors.