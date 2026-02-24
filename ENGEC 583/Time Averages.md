Why do we do time averages? What even is a time average?
$$A_{RMS}=\sqrt{\frac1T\int_0^Tdt(A_M(t))^2}$$
For a sinusoidal signal:
$$A_{RMS}=A_M\sqrt{\frac1T\int_0^Tdt(\sin\omega t)^2}$$
$$=A_M\sqrt{-\frac1{4T}\int_0^Tdt(e^{j\omega t}-e^{-j\omega t})^2}$$
$$=A_M\sqrt{-\frac1{4T}\int_0^Tdt[e^{2j\omega t}+e^{-2j\omega t}-2]}$$
$$=A_M\sqrt{\frac1{2T}\int_0^Tdt[1-\cos2\omega t]}$$
$$=A_M\sqrt{\frac T{2T}}$$
$$=A_M/\sqrt{2}$$
For a given duty cycle ($t_{on}=U=DT$):
$$A_{RMS}=A_M\sqrt{\frac1T\int_0^Udt+\frac1T\int_U^T0}$$
$$=A_M\sqrt{\frac U T}$$
$$=A_M\sqrt{D}$$
> aside: the issue with space solar satellites is that the atmosphere which blocks us from much of the UV waves, also blocks us from sending energy down to earth. there are CHARGED PARTICLES in the atmosphere, which means a lot of *weirdness* happens when you try sending EM waves through. electrons get excited more due to less mass and the ions start to move around. some things change: (temperature, density, earth's magnetic field). changing the magnetic field has baaaaad ecological effects. but there's actually a threshold for it???

