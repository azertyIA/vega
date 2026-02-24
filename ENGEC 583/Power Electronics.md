![[Pasted image 20260210150613.png]]
What does that DC power supply do in the lab? It just seems like some random, magical tool that we use to test our circuits. This is the basic DC adapter circuit. It's good for most things, but not for very heavy duty.
1. **transformer**: converts big AC into little AC and disconnects you (dc) from mains (ac).
2. **rectifier**: puts an absolute value function on the AC.
3. **filterer**: takes out the higher frequency voltage (smooths)
4. **regulator**: further smooths to breakdown voltage of the diode.

There are two conditions to turn linear inductors into an ideal transformer:
1. perfect coupling: $v_1N_2=v_2N_1$
2. no power loss: $v_1i_1=v_2i_2$


![[Pasted image 20260212145926.png]]
The Zener diode has some impurities to create a breakdown voltage. Beyond this breakdown voltage, it can behave as a diode in the other direction. To find the efficiency of the converter you can use the following formula:
$$\text{Efficiency}=P_L/(P_L+P_T)$$
Dissipated power ($P_T$) is usually a result of a resistor. But any circuit element can be associated with having current go through it and voltage go across it. 