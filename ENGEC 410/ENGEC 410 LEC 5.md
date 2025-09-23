## DC Power Supplies

DC Power Supplies usually use transformers to turn AC into a different voltage. Then the voltage goes into a diode rectifier to turn the sines into absolute sines. Then it goes into a filter to smooth out the bumps before hitting a voltage regulator. Then it arrives at the load.
> ac source > transformer > rectifier > filter > regulator > load

### Diode Rectifier

A normal diode rectifier only lets positive signals through. Half-wave and Full-wave rectifiers exist. A typical half-wave rectifier setup features a diode and a resistor, and assuming a constant voltage drop will basically do: 
> $\max(0,\cos\omega t-V_0)$

If you flip the diode, you'll just get the negative part. If you include both, then you'll get:
> $\max(0,|\cos\omega t|-V_0)$

### Filter Capacitor
The filter capacitor takes the voltage and pushes it through a diode and putting it in a capacitor-like loop, stabilizing the voltage with time factor RC.

### Voltage Regulator
The source gets connected to a resistor which branches into a Zener diode to ground and a resistor to ground. The result voltage is the voltage across the resistor load.

In the case of no load ($R_L=0$), the current going through the start is what goes through the diode.
> $I=I_Z=\frac{V_S-V_Z}{R+r_z}$

If $V_S$ changes by $\Delta$:
> $V=V_Z+\frac{(V_S+\Delta-V_Z)r_Z}{R+r_Z}$

As long as $R>>r_Z$, $\Delta\to0$.

### Limiter Circuit
A good limiter circuit should look like a sigmoid but linear. But it doesn't matter as long as it works. You could use two Zener diodes facing each other for such a circuit.

### Clamped Capacitor
A clamped capacitor has a $V_O=V_I+V_C$. It basically offsets the voltage by some amount.

## MOSFET
MOSFET stands for Metal Oxide Semiconductor Field Effect Transistor. $V_G$ contributes drift current across $S\to D$. 