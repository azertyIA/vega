
![[IMG_0006.jpeg]]
Transmission lines feature three types:
1. Parallel-plate (printed circuit)
2. Two-wire (telephone line)
3. Coaxial (power cables)

## Parallel Plates
Imagine an infinitely long plate (or two), and the conductivity of these plates goes to infinity. The wave propagates along each strip, $\vec H$ goes across the strip's width and $\vec E$ goes across the dielectric. But what causes electric fields other than the separation of charge? When a cloud is charged, it builds a massive electric charge across the atmosphere with free electrons. It builds up until breakdown occurs and lightning strikes. What happened to typing out equations?

Basically a capacitor can be a Zener diode if you try hard enough. So, charge will be induced. Magnetic fields induce a current longitudinally. The circuit symbol for transmission lines looks like two wires as seen in the picture (II). To make a circuit you need a source (with impedance) and a load (is impedance). Source end and load end represent the voltages across the source and volt (just so you get cause and effect). The interface circuit is the TLs here.

![[IMG_0007.jpeg]]
The equivalent circuit has a few components. $R_C$ comes from the resistance of the conductor, $(G_m)R_m$ represents the resistance of the dielectric. $C$ and $L$ are a little more obvious. The top current has $i(z,t)$ with end being $i(z+\Delta z,t)$ where $\Delta z$ represents the coordinate change: the length.

All of these are in $\Omega/m$ (R), $H/m$ (L), $F/m$ (C), and $S/m$ (G) (Siemen = 1 / Ohm). If the length was zero then everything would be zero. So, that's why it's in these kind of units.

Kirchhoff Voltage Law under AC steady state:
> $V(z,t)-Ri(z,t)\Delta z-L\partial_ti(z,t)\Delta z=V(z+\Delta z,t)$
> $-Ri(z,t)\Delta z-L\partial_ti(z,t)\Delta z=\Delta V(z,t)$
> $\partial_z V(z,t)=-Ri-L\partial_ti$
> $-\partial_z V(z,t)=(R+L\partial_t)i$
> $jkV=(R+j\omega L)i$

Kirchhoff Circuit Law under AC steady state:
> $i(z,t)=i_G+i_C+i(z+\Delta z,t)$
> $i(z,t)=GV_G\Delta z+C\partial_tV\Delta z+i(z+\Delta z,t)$
> $\partial_zi(z,t)=-GV_G-C\partial_tV_C$
> $-\partial_zi(z,t)=(G+C\partial_t)V$
> $jki=(G+j\omega C)V$

Unify them into one equation:
> $jkV=(R+j\omega L)i$
> $i=\frac1{jk}(G+j\omega C)V$
> $-k^2V=(R+j\omega L)(G+j\omega C)V$
> $-k^2=(RG+j\omega(LG+RC)-\omega^2 LC)$
> $k^2=(\omega^2 LC-RG-j\omega(LG+RC))$

In a more general sense:
> $-\partial_z V(z,t)=(R+j\omega L)i$
> $-\partial_zi(z,t)/(G+j\omega C)=V$
> $\partial_z^2i(z,t)/(G+j\omega C)=(R+j\omega L)i$
> $\partial_z^2i(z,t)=(R+j\omega L)(G+j\omega C)i$
> $k^2=(R+j\omega L)(G+j\omega C)$
> $k^2=-\omega^2 LC$ (lossless)
> $LC=\mu\epsilon$ (lossless)

When actually used in a circuit there is often a source voltage, a source resistance, and a load impedance.

> $V(z)=V_+e^{-\gamma z}+V_-e^{+\gamma z}$ (a linear combination of the lossless case eigenvalues)
> $I(z)=I_+e^{-\gamma z}+I_-e^{+\gamma z}$
> $-\partial_z V(z,t)=(R+j\omega L)i$
> $\gamma V=(R+j\omega L)I$
> $[\gamma V_+-(R+j\omega L)I_+]e^{-\gamma z}=[\gamma V_-(R+j\omega L)I_-]e^{+\gamma z}$ for all z
> $\to[\gamma V_+-(R+j\omega L)I_+]=0$
> $\to[\gamma V_-+(R+j\omega L)I_-]=0$
> $\to Z=V_+/I_+=-V_-/I_-=R+j\omega L/\gamma$
> $=\sqrt{R+j\omega L/G+j\omega C}$
> $=\sqrt{L/C}=R_0+jX_0$ (lossless)
> $v_{ph}=\omega/\beta=1/\sqrt{LC}$

