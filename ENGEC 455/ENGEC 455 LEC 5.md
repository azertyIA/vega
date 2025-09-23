Ooh, homework time. Don't forget that cover page.
## Faraday's Law
Faraday's Law is described as such:
> $\nabla\times\vec{E}=-\partial_t\vec{B}$

Two resistors. Seven ohms and three ohms in a loop. A magnetic field flows into the page. The E and B field both are functions of space and time. Don't worry about the minus sign. But if you wanted to care: it's just another vector surface thing.

We can convert this differential form of Faraday's law into integral form using Stoke's theorem. So we can use this contour of the loop (or the loop) and the area of the loop.
> $=\int d\vec{s}\cdot(\nabla\times\vec{E})=-\partial_t\iint d\vec{s}\cdot\vec{B}$
> $=\oint d\vec{l}\cdot\vec{E}=-\partial_t\Phi_B$

The negative sign is called *Lenz' Law*. Imagine you're in a car and you accelerate or decelerate, your inertia is what pulls you back or forward. Mother nature hates sudden change. Inertia is just one example. Diffusion and Lorentz force is another example.
> If you drag a conducting wire across a magnetic field, then charge will start accumulating to each end. The act of moving the charge produces a current and thus a magnetic field. That opposes the background field.

In the N junction, you put group 5 atoms (P/As/Bi), which put an extra electron that can't bind to the surrounding silicon atoms, representing free electrons. In the P junction you put group 3 atoms (Al/B) which contain "electron holes."

Electrons from the N block will try to diffuse into the P block. The P block will have extra electrons than neutral with negative ions, and the N block will have extra holes than neutrals with positive ions. So, an electric field is produced pointing from the positive ion block to the negative ion block.

For a $V_S$ in a loop with a resistor, a current is produced, adding a magnetic field. So Lenz' Law has a minus sign because it tries to RESIST a changing current making a magnetic field.

So no answer I guess.

Let's put a loop in it. Now $n=2$ in turns. Now that we have an extra loop, the induced voltage will be doubled, because the line integral will have "double the length." If we try to find the voltage across the 3 Ohm resistor (ad), then we have to make a loop of the three ohm resistor and the voltmeter. There is no magnetic field in the middle of that, so it should be normal: 0.3V.  Alternatively, the 7 Ohm resistor (bc), measures a 0.7V voltage difference, However, if you make you voltmeter probes include the magnetic field, then you have to add one additional volt.
> A voltmeter just has a super big resistance. Very little current flows through the voltmeter, just to measure without messing up the measurement.
## Ampere's Law

Take one piece of a closed loop of wire with some radius $a$ so you get a cylinder. There is a current flowing through it. Now there are two things to consider:
> $\nabla\times\vec{H}=\vec{J}_c+\partial_t\vec{D}$

If something has infinite resistance, then "no current" would flow through. This is known as an open circuit. Just cut the wire? Meanwhile, zero resistance is created by a short circuit.

Anyways integral form lmao:
> $\iint d\vec{s}\cdot(\nabla\times\vec{H})=\iint d\vec{s}\cdot\vec{J}+\partial_t\iint d\vec{s}\cdot\vec{D}$
> $\iint d\vec{s}\cdot(\nabla\times\vec{H})=I_{enc}+\partial_t\Phi_D$
> $2\pi rH=\oint d\vec{s}\cdot\vec{H}=I_{enc}+\partial_t\Phi_D$

Alternate version of Ohm's Law:
> $\vec{J}=\sigma\vec{E}\to I=(1/R)*V$, but differential.

Here, there is no time variant electric field, so we can get rid of the final term. So, we're just left with the fact that the current induces a magnetic field of strength depending on how the contour is drawn.
> $H=\frac{I}{2\pi r}$