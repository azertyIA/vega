The **transfer characteristics** describes the input signal in the context of its effect on the output signal. For example, two resistors might voltage divide the input voltage to create the output voltage. 

### Clipping and Limiting
Or if the diode is dividing the input to ground, you might get a slope before a straight line.

![[Pasted image 20260225201129.png]]
This leads to clipping and limiting, or when the characteristic activates or deactivates a diode (probably deactivate though). The equivalent circuit you can make with this involves replacing the diode with either an open circuit or a voltage source and a resistor. 

In all aspects, the current going through the resistor must not be contrary to where the diode was originally pointed. As a result, the formula might look like:
$$v_{OUT}=V_f+\frac{r_d}{R_1+R_d}(v_{IN}-V_f)$$
If the in voltage was less than the activation voltage, then the diode would be making mysterious current, so the formula no longer applies. What about the other diode though?

![[Pasted image 20260225201849.png]]
That would require the input voltage to be less than the negative activation voltage. Then, the formula for that case would be:
$$v_{OUT}=-V_f+\frac{r_d}{R_1+R_d}(V_f+v_{IN})$$
It wouldn't be completely flat, but the gain would drop dramatically on both extremes. So what do we do if we wanted more customization?

What we could do to modify it is put voltage sources near the diodes, letting you move the activation voltage to different levels, because you would need a higher or lower voltage to trigger the diode. You can also use a zener diode which has three modes of activation:

![[Pasted image 20260225202510.png]]
As can be seen, it's a regulator that clips in both directions, with different cutoff points and gains. And so, instead of having a voltage source opposing the diode, you could instead just have one of these zener diode face against the diode for the same effect. But if you put two zener into each other, you could get a symmetric effect and not need more than two diodes.
### Rectifiers
If you instead put the diodes in the top rather than a resistor you can now rectify out an entire voltage set after the zero point. If the input voltage does not overcome the activation voltage, the circuit is left incomplete, but otherwise the voltage grows normally.
