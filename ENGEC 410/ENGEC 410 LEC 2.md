Last time we talked about resistors, capacitors, and inductors.
> $V=IR$
> $Q=CV$
> $V=L\partial_tI$

Kirchhoff Laws state how circuits work:
> KCL (junction): $\sum i=0$
> KVL (loop): $\sum v=0$

Thevenin equivalent circuits turn linear circuits into a voltage source and a resistor.
> $V_{th}$: open-circuit voltage at terminals
> $R_{th}$: resistance at terminal with power sources turned off

Signals can fluctuate with time. It could either be analog or digital.
> Ex: $v(t)=A\sin\omega t$, $i(t)=1+u_2(t)$

You can get frequency-dependent response using the Fourier Transform, such that any function can be expressed in terms of sines and cosines:
> $f(\omega)=\int dtf(t)e^{-i\omega t}$
> $f(t)=\int d\omega f(\omega)e^{+i\omega t}$

For discrete functions use summation notation instead. For example, we usually see a "pulse" that has a signal persist for some time. This would be Fourier Transformed to a sine packet:
> $f(\omega)=\frac{2\sin\omega t}{\omega}$

An amplifier can increase the magnitude of voltage on a signal.
> $A_v=v_o/v_i$
> $A_i=i_o/i_i$
> $A_p=i_ov_o/i_iv_i=A_iA_v$

These gains are classically unitless but we still write them in *decibels*:
> $1db=20\log A$

Amplifier saturation occurs when there isn't anymore gain. This happens because the amplifier is operated and bound by two different power sources. This leads to a sort of sigmoid shape.

Amplifiers are usually composed of transistors which is due to device physics. Transistors are sandwiched doped silicon. Semiconduction works because the conductive electrons hover just above the top valence electrons and it just works out. 

If you add electrons to the valence shell then you get n-types (electron in conduction), otherwise you get p-types (holes in valence). These correspond to group V and III. Holes move with the electric field while electrons move against the electric field.

Putting a p-doped and n-doped material together you get a diode. Orienting the electric field to pull the electrons and holes closer to each other causes a recombination current that allows for conduction. Otherwise, the electric field will push apart the electrons and holes causing a "dead zone."