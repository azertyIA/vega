There are two important theorems to use for this course: Divergence Theorem (Gauss' Theorem), and Stoke's Theorem.

Divergence Theorem: 
> You arbitrarily select a region that encapsulates a 3D volume $V$ before determining that the "total divergence" of said volume is the total flux of the surface $\vec{S}$.

Flux doesn't really have a good definition for itself, but we know what it is: some current going through a surface. Mosquitoes, water, electrons, etc.

Current density $\vec{J}$ is measured in "current" per area. (stuff/time-area) Let's take a look at an equation:
> Ampere's Law: $\nabla\times\vec{H}=\vec{J}+\partial_t\vec{D}$

If a ton of mosquitoes get trapped in a volume, then the flux will have to had increased:
> $\partial_t Q=\oint_\vec{S}d\vec{s}\cdot\vec{J}$

But, Q can be written in the form of stuff density:
> $Q=\int_VdV\rho$
> $\partial_t\int dV\rho=\oint d\vec{s}\cdot\vec{J}$

What does the dot product mean though? It has a formula:
> $\vec{A}\cdot\vec{B}=AB\cos\theta_{AB}$, a scalar.
> $\vec{A}\times\vec{B}$, on the other hand gives you a vector.

A closed surface should be specified as *outward* and *normal*. So if $\vec{J}$ points inward into the volume, you'll get a negative dot product. Or, inward flux is negative and positive otherwise.

Divergence theorem says:
> $\oint_Sd\vec{s}\cdot\vec{J}=\int dV(\nabla\cdot\vec{J})$
> Keep in mind that the $\vec{\nabla}$ is a actually a vector to represent gradient-ish.

So, it can be rewritten using the Divergence theorem. 
> $\int dV\partial_t\rho=\oint_Sd\vec{s}\cdot\vec{J}=\int dV(\nabla\cdot\vec{J})$
> $\int dV(\partial_t\rho-\nabla\cdot\vec{J})=0$

Now that you can select any volume, then any volume will be zero, even the integrand.
> $\partial_t\rho-\nabla\cdot\vec{J}=0$

However, a positive flux has things going outwards, so how can a positive, outward flux be equal to an increasing amount of "stuff" in a volume? How can stuff be increasing if it's all going out? 

To fix this, the current density relation needs to be negative, resulting in the real equation:
> Continuity Equation: $\partial_t\rho+\nabla\cdot\vec{J}=0$

Whereas Divergence Theorem deals with closed surfaces and encapsulated volumes, Stoke Theorem tells you about open surfaces:
> $\oint_rd\vec{l}\cdot\vec{E}=\int d\vec{s}\cdot(\nabla\times\vec{E})$
