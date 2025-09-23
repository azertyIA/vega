Diode has a specific IV equation:
> $I=I_s(e^{eV/k_BT}-1)$ (an offset exponential)

Diode on says that current forward biases from triangle to the line, or from the p-doped silicon to the n-doped silicon. Meanwhile, diode off says that current reverse biases from the line to the triangle.

There are a few models:
> $I=I_se^{eV/k_BT}$ (pure exponential, difficult to solve)
> $I\in{0,\infty}$ (ideal diode, simple but mere approximate) (wire)
> $I(V\approx0.7)\in{0,\infty}$ (constant voltage drop, also approximate) (battery)
> $I=\frac{1}{r_d}(V-V_{D0})>0$ (linear model, approximates exponential) (battery + resistor)
> $I=I_seV/nk_BT$ (small signal, exponential expansion, $n$ realism) (resistor)

Diode examples:
> A 5V source goes into a resistor (5kO) which splits into two diodes on the left and right. The left diode exits to ground while the right diode exits to (V) and a resistor (10kO) which exits to a -5V source.

If the diodes are perfectly ideal, then V is 0 and the current through the right diode:
> $I_{R}=\frac{5V}{10k\Omega}=0.5mA$
> $I_{in}=\frac{5V}{5k\Omega}=1mA$
> $I_L=I_{in}-I_R=0.5mA$

Next one:
> A 9V source goes into a resistor (10kO) which branches left and right. Left has a resistor (20kO) which goes to ground. Right has a diode which branches to a resistor (20kO) and a voltage source (v).

Let's talk about Zener diodes a little bit more. Zener diodes can breakdown via electron quantum tunnelling. It just works like that. Electrons are waves anyways. It looks like two lines when zoomed out.
> The x-intercept is $V_{Z0}$
> The start of linear increase in current is $V_{Zk}$
> They should be the almost the same if it's a good transistor with a small saturation current.

Zener diodes can be treated as a voltage source ($V_{Z0}$) and a resistor ($r_Z$) in series.