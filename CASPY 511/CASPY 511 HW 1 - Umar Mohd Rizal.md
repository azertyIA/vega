#PY511
# 1. Homework 1
## 1.0. Nature Quantum Quiz and Survey

i. Write down how Nature's AI-bot classified your belief.
> Nature's AI-bot classified my belief with the Copenhagen interpretation.

ii. Describe briefly at least one of the alternative views to the Copenhagen interpretation
> The other most popular belief is the many worlds interpretation, wherein if there is a chance of something happening differently due to the nature of quantum mechanics, then an entirely new universe is created in parallel to simulate that possibility. 

## 1.1. Fundamental Constants

### 1.1.a. Today's Standards

**I want to measure the speed of light (c) using Fizeau's method.**

You are measuring the meter. The speed of light was fixed to $299792458$ m/s and the second was fixed to the hyperfine transition frequency of the Cesium-133 isotope being 9.192631770 GHz.

**I want to measure Planck's constant (h) using the Photoelectric Effect.**

You are measuring the volt. The electron already has a charge (as is seen later) and as mentioned previously the second is fixed. The related equation is $eV=h\nu+\phi$. By trying to measure the slope of this relation, you also have to rely on measuring by the volt in order to get the energy difference across different frequencies.

**I want to measure Avogadro's number (N) by counting the number of moles in a gram of pure carbon.**

You are measuring the gram. Avogadro's number has been set to a fixed number, and by collecting that many "moles" in a gram, you effectively measure the amount of carbon in a gram, or how a gram relates to atomic units.

**I want to measure the Boltzmann constant (k) using an analysis of Brownian motion of polystyrene microspheres in water**

You are measuring the Kelvin. The related equation is $\braket{x^2}=\frac{2k_BT}{\gamma}t$ and since $k_B$ is fixed, what you really measure by is the temperature (kelvin).

**I want to measure the magnitude of the electron charge (e) using the Millikan's Oil Drop method.**

You are measuring the Coulomb as the coulomb used to be defined, but now relies on the charge of the electron since 2019. $e=1.609*10^{-19}$ C.

**How would your responses change before 2019?**

Since the meter was the only one defined before the standard fixing, only that response would not change. Many of the units seen to be measured here used to have definitions like the Avogadro's number in a near perfect sphere of Silicon. Meanwhile, the International Prototype Kilogram used to define the kilogram, so constants that use energy units (like h, that uses volts) could actually be measured in relation to that prototype. Furthermore, the electron charge used to be an experimental value. 

## 1.2. Linear Algebra

>$\sigma_x=\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}$, $\sigma_y=\begin{pmatrix}0 & -i \\ i & 0\end{pmatrix}$, $\sigma_z=\begin{pmatrix}1 & 0 \\ 0 & -1\end{pmatrix}$

To preface, messing around with these matrices lends to some very fun properties:
> Squaring any Pauli spin matrix gets you the identity matrix: $\sigma_\mu^2=I$
> They anti-commute: $\sigma_\mu\sigma_\nu=-\sigma_\nu\sigma_\mu$

One other trick is that when multiplied in x-y-z-x chirality, they result in in $i$ multiplied with the other Pauli spin matrix. Otherwise you get the negative.

a.i. $\sigma_x\sigma_y$
> $=\sigma_z$ (positive chirality)

a.ii. $[\sigma_y,\sigma_z]$
> $=\sigma_y\sigma_z-\sigma_z\sigma_y$ (positive - negative chirality)
> $=i\sigma_x+i\sigma_x$
> $=2i\sigma_x$

a.iii. $\sigma_x\sigma_y\sigma_z$
> $=i\sigma_z\sigma_z$ (positive chirality)
> $=iI$ (squared to identity)

b.i. $\sigma_+=\sigma_x+\sigma_y$
> $=\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}+i\begin{pmatrix}0 & -i \\ i & 0\end{pmatrix}$
> $=\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}+\begin{pmatrix}0 & 1 \\ -1 & 0\end{pmatrix}$
> $=\begin{pmatrix}0 & 2 \\ 0 & 0\end{pmatrix}$
 >$\begin{pmatrix}0 & 2 \\ 0 & 0\end{pmatrix}^\dagger=\begin{pmatrix}0 & 0 \\ 2 & 0\end{pmatrix}\neq\begin{pmatrix}0 & 2 \\ 0 & 0\end{pmatrix}$
 > $\sigma_+$ is not Hermitian.

b.ii. $\sigma_-=\sigma_x-\sigma_y$
> $=\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}-i\begin{pmatrix}0 & -i \\ i & 0\end{pmatrix}$
> $=\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}+\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}$
> $=\begin{pmatrix}0 & 0 \\ 2 & 0\end{pmatrix}$
 >$\begin{pmatrix}0 & 0 \\ 2 & 0\end{pmatrix}^\dagger=\begin{pmatrix}0 & 2 \\ 0 & 0\end{pmatrix}\neq\begin{pmatrix}0 & 0 \\ 2 & 0\end{pmatrix}$
 > $\sigma_-$ is not Hermitian.

c.i. $\sigma_x:\lambda,\vec{v}=?$
> $\det(\sigma_x-\lambda I)=0$
> $\det\begin{pmatrix}-\lambda & 1 \\ 1 & -\lambda\end{pmatrix}=0$
> $\lambda^2-1=0$
> $\lambda=\pm1$
> $\lambda_{-1}:\begin{pmatrix}1 & 1 \\ 1 & 1\end{pmatrix}\begin{pmatrix}v_1 \\ v_2\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix},v_1=-v_2$
> $\vec{v}_{\lambda=-1}=\begin{pmatrix}1 \\ -1\end{pmatrix}$
> $\lambda_{1}:\begin{pmatrix}-1 & 1 \\ 1 & -1\end{pmatrix}\begin{pmatrix}v_1 \\ v_2\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix},v_1=v_2$
> $\vec{v}_{\lambda=1}=\begin{pmatrix}1 \\ 1\end{pmatrix}$

c.ii. $\sigma_y\lambda,\vec{v}=?$
> $\det(\sigma_y-\lambda I)=0$
> $\det\begin{pmatrix}-\lambda & -i \\ i & -\lambda\end{pmatrix}=0$
> $\lambda^2-1=0$
> $\lambda=\pm1$
> $\lambda_{-1}:\begin{pmatrix}1 & -i \\ i & 1\end{pmatrix}\begin{pmatrix}v_1 \\ v_2\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix},v_1=iv_2$
> $\vec{v}_{\lambda=-1}=\begin{pmatrix}1 \\ -i\end{pmatrix}$
> $\lambda_{1}:\begin{pmatrix}-1 & -i \\ i & -1\end{pmatrix}\begin{pmatrix}v_1 \\ v_2\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix},v_1=-iv_2$
> $\vec{v}_{\lambda=1}=\begin{pmatrix}1 \\ i\end{pmatrix}$

c.iii. $\sigma_z:\lambda,\vec{v}=?$
> $\det(\sigma_z-\lambda I)=0$
> $\det\begin{pmatrix}1-\lambda & 0 \\ 0 & -1-\lambda\end{pmatrix}=0$
> $\lambda^2-1=0$
> $\lambda=\pm1$
> $\lambda_{-1}:\begin{pmatrix}2 & 0 \\ 0 & 0\end{pmatrix}\begin{pmatrix}v_1 \\ v_2\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix},v_1=0,v_2$ unbounded
> $\vec{v}_{\lambda=-1}=\begin{pmatrix}0 \\ 1\end{pmatrix}$
> $\lambda_{1}:\begin{pmatrix}0 & 0 \\ 0 & -2\end{pmatrix}\begin{pmatrix}v_1 \\ v_2\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix},v_2=0,v_1$ unbounded
> $\vec{v}_{\lambda=1}=\begin{pmatrix}1 \\ 0\end{pmatrix}$

d: $[\sigma_x,[\sigma_y,\sigma_z]]+[\sigma_y,[\sigma_z,\sigma_x]]+[\sigma_z,[\sigma_x,\sigma_y]]$
> $=[\sigma_x,2i\sigma_x]+[\sigma_y,2i\sigma_y]+[\sigma_z,2i\sigma_z]$ (positive chirality)
> $=2i\sigma_x^2-2i\sigma_x^2+\dots$ (sigma matrices commutes with itself)
> $=0+0+0=0$

## 1.3. Exponentials of Operators

> $e^A=\Sigma\frac{1}{n!}A^n,\sigma^2=1$
> $\Sigma_{even}\frac{1}{n!}(i\theta)^n=0-x^2/2+x^4/24+\dots=\cos\theta$
> $\Sigma_{odd}\frac{1}{n!}(i\theta)^n=i(x+-x^3/6+\dots)=i\sin\theta$

For the first set of (a) problems, I'll be using the fact that Pauli matrices square to the identity, so the infinite sum can be split into two cases, even and odd. This can simplify down to simple trig functions if manipulated in the correct fashion.

a.i: $e^{i\theta\sigma_z}$
> $=\Sigma\frac{1}{n!}(i\theta\sigma_z)^n$
> $=\Sigma_{even}\frac{1}{n!}(i\theta)^nI+\Sigma_{odd}\frac{1}{n!}(i\theta)^n\sigma_z$
> $=\begin{pmatrix}\Sigma_{even}\frac{1}{n!}(i\theta)^n & 0 \\ 0 & \Sigma_{even}\frac{1}{n!}(i\theta)^n\end{pmatrix}+\begin{pmatrix}\Sigma_{odd}\frac{1}{n!}(i\theta)^n & 0 \\ 0 & -\Sigma_{odd}\frac{1}{n!}(i\theta)^n\end{pmatrix}$
> $=\begin{pmatrix}\Sigma_{even}\frac{1}{n!}(i\theta)^n+\Sigma_{odd}\frac{1}{n!}(i\theta)^n & 0 \\ 0 & \Sigma_{even}\frac{1}{n!}(i\theta)^n-\Sigma_{odd}\frac{1}{n!}(i\theta)^n\end{pmatrix}$
> $=\begin{pmatrix}\Sigma_{even}\frac{1}{n!}(i\theta)^n+\Sigma_{odd}\frac{1}{n!}(i\theta)^n & 0 \\ 0 & \Sigma_{even}\frac{1}{n!}(-i\theta)^n+\Sigma_{odd}\frac{1}{n!}(-i\theta)^n\end{pmatrix}$
> $=\begin{pmatrix}\Sigma\frac{1}{n!}(i\theta)^n & 0 \\ 0 & \Sigma\frac{1}{n!}(-i\theta)^n\end{pmatrix}$
> $=\begin{pmatrix}e^{i\theta} & 0 \\ 0 & e^{-i\theta}\end{pmatrix}$

a.ii: $e^{i\theta\sigma_x}$
> $=\Sigma\frac{1}{n!}(i\theta\sigma_x)^n$
> $=\Sigma_{even}\frac{1}{n!}(i\theta)^nI+\Sigma_{odd}\frac{1}{n!}(i\theta)^n\sigma_x$
> $=\begin{pmatrix}\Sigma_{even}\frac{1}{n!}(i\theta)^n & 0 \\ 0 & \Sigma_{even}\frac{1}{n!}(i\theta)^n\end{pmatrix}+\begin{pmatrix}0 & \Sigma_{odd}\frac{1}{n!}(i\theta)^n \\ \Sigma_{odd}\frac{1}{n!}(i\theta)^n & 0\end{pmatrix}$
> $=\begin{pmatrix}\Sigma_{even}\frac{1}{n!}(i\theta)^n & \Sigma_{odd}\frac{1}{n!}(i\theta)^n \\ \Sigma_{odd}\frac{1}{n!}(i\theta)^n & \Sigma_{even}\frac{1}{n!}(i\theta)^n\end{pmatrix}$
> $=\begin{pmatrix}\cos\theta & i\sin\theta \\ i\sin\theta & \cos\theta\end{pmatrix}$

a.iii: $e^{i\theta\sigma_y}$
> $=\Sigma\frac{1}{n!}(i\theta\sigma_x)^n$
> $=\Sigma_{even}\frac{1}{n!}(i\theta)^nI+\Sigma_{odd}\frac{1}{n!}(i\theta)^n\sigma_x$
> $=\begin{pmatrix}\Sigma_{even}\frac{1}{n!}(i\theta)^n & 0 \\ 0 & \Sigma_{even}\frac{1}{n!}(i\theta)^n\end{pmatrix}+\begin{pmatrix}0 & -i\Sigma_{odd}\frac{1}{n!}(i\theta)^n \\ i\Sigma_{odd}\frac{1}{n!}(i\theta)^n & 0\end{pmatrix}$
> $=\begin{pmatrix}\Sigma_{even}\frac{1}{n!}(i\theta)^n & -i\Sigma_{odd}\frac{1}{n!}(i\theta)^n \\ i\Sigma_{odd}\frac{1}{n!}(i\theta)^n & \Sigma_{even}\frac{1}{n!}(i\theta)^n\end{pmatrix}$
> $=\begin{pmatrix}\cos\theta & \sin\theta \\ -\sin\theta & \cos\theta\end{pmatrix}$

b. $\sigma_+,\sigma_-$
> $\sigma_+=\begin{pmatrix}0 & 2 \\ 0 & 0\end{pmatrix}$
> $\sigma_-=\begin{pmatrix}0 & 0 \\ 2 & 0\end{pmatrix}$
> $\sigma_+^2=\sigma_-^2=0$

b.i. $e^{i\theta\sigma_+}$
> $=\Sigma\frac{1}{n!}(i\theta\sigma_+)^n$
> $=I+i\theta\sigma_++0$
> $=\begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix}+\begin{pmatrix}0 & 2i\theta \\ 0 & 0\end{pmatrix}$
> $=\begin{pmatrix}1 & 2i\theta \\ 0 & 1\end{pmatrix}$

b.ii. $e^{i\theta\sigma_-}$
> $=\Sigma\frac{1}{n!}(i\theta\sigma_-)^n$
> $=I+i\theta\sigma_-+0$
> $=\begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix}+\begin{pmatrix}0 & 0 \\ 2i\theta & 0\end{pmatrix}$
> $=\begin{pmatrix}1 & 0 \\ 2i\theta & 1\end{pmatrix}$

c.i. $e^{i\theta\sigma_+}\sigma_ze^{-i\theta\sigma_+}$
> $=\begin{pmatrix}1 & 2i\theta \\ 0 & 1\end{pmatrix}\begin{pmatrix}1 & 0 \\ 0 & -1\end{pmatrix}\begin{pmatrix}1 & -2i\theta \\ 0 & 1\end{pmatrix}$
> $=\begin{pmatrix}1 & -2i\theta \\ 0 & -1\end{pmatrix}\begin{pmatrix}1 & -2i\theta \\ 0 & 1\end{pmatrix}$
> $=\begin{pmatrix}1 & -4i\theta \\ 0 & -1\end{pmatrix}$

c.i. $e^{-i\theta\sigma_-}\sigma_ze^{i\theta\sigma_+}$
> $=\begin{pmatrix}1 & 0 \\ -2i\theta & 1\end{pmatrix}\begin{pmatrix}1 & 0 \\ 0 & -1\end{pmatrix}\begin{pmatrix}1 & 2i\theta \\ 0 & 1\end{pmatrix}$
> $=\begin{pmatrix}1 & 0 \\ -2i\theta & -1\end{pmatrix}\begin{pmatrix}1 & 0 \\ 2i\theta & 1\end{pmatrix}$
> $=\begin{pmatrix}1 & 0 \\ -4i\theta & -1\end{pmatrix}$

d.i $(\vec{a}\cdot\vec{\sigma})(\vec{b}\cdot\vec{\sigma})$
> $(a_x\sigma_x+a_y\sigma_y+a_z\sigma_z)(b_x\sigma_x+b_y\sigma_y+b_z\sigma_z)$
> $=\Sigma a_nb_n\sigma_n^2+i(a_yb_z-a_zb_y)\sigma_x+i(a_zb_x-a_zb_x)\sigma_y+i(a_xb_y-a_yb_x)\sigma_z$

The first term is has squared sigma matrices (identity), so that's just the dot of a and b. All the subtractions represent the cross product, the sigma matrices represent the sigma vector, so they can be dotted.
> $=(\vec{a}\cdot\vec{b})I+i(\vec{a}\times\vec{b})\cdot\sigma$

d.ii $[\vec{a}\cdot\vec{\sigma},\vec{b}\cdot\vec{\sigma}]$
> $=(\vec{a}\cdot\vec{\sigma})(\vec{b}\cdot\vec{\sigma})-(\vec{b}\cdot\vec{\sigma})(\vec{a}\cdot\vec{\sigma})$
> $=(\vec{a}\cdot\vec{b})I+i(\vec{a}\times\vec{b})\cdot\vec{\sigma}-(\vec{b}\cdot\vec{a})I-i(\vec{b}\times\vec{a})\cdot\vec{\sigma}$

Dot product commutes and cross product anti-commutes.
> $=(\vec{a}\cdot\vec{b})I+i(\vec{a}\times\vec{b})\cdot\vec{\sigma}-(\vec{a}\cdot\vec{b})I+i(\vec{a}\times\vec{b})\cdot\vec{\sigma}$
> $=2i(\vec{a}\times\vec{b})\cdot\vec{\sigma}$

## 1.4. Cheap Cigars

### 1.4.a. Control
Explain what the control photograph is showing.
> The control photograph is showing the (lack of) impact the magnetic field has on the silver atoms; the atoms are originally shot in a ray towards the sheet to draw a line. There are no current forces pushing the atom away from drawing just a line.

### 1.4.b. Magnetic Moment
**Estimate the maximum deflection of the silver atoms from the photograph.** 
> The maximum deflection of the silver atoms (measuring from the edge of the lips to the lower "lip") looks to be about 2 tick marks, which corresponds to 100 microns.

**From this, estimate the magnetic moment of the electron.** 

For calculations, we are given a few things:
- $T=1273.15$ K
- $l_{beam}=3.5$ cm
- $B_0=0.1$ Tesla (unneeded)
- $\partial_zB=10$ Tesla / cm

Obviously, the silver atom is subject to the magnetic gradient for some amount of time as the sole force for deflection. So, to figure out how long it spent, divide the length of the beam by the unaltered velocity component through the magnet:
> $t=l_{beam}/v$

Velocity can be found by using the Boltzmann speed distribution:
> $\frac{1}{2}mv^2=\frac{3}{2}k_BT$
> $v=\sqrt{3k_BT/m}$
> $t=l_{beam}\sqrt{m/3k_BT}$

Now that we have the time, let's find the force experienced during the magnetic field:
> $\vec{F}=\nabla(\vec{m}\cdot\vec{B})$, the magnetic moment is just a scalar here.
> $F_z=\partial_z(\mu\vec{B})$
> $F_z=\mu\partial_zB$

Putting them together:
> $\Delta x=\frac{1}{2}Ft^2/m$
> $\Delta x=(0.5)(\mu\partial_zB)(l_{beam}^2m/3k_BT)(1/m)$, mass is canceled

Solving for $\mu$:
> $\mu=6(\Delta xk_BT)/(\partial_zBl^2)$
> $=8.6\times10^{-24}$ Joules / Tesla

**Why is the magnetic moment of the Silver atom just the magnetic moment of a single electron?**

The magnetic moment of the Silver atom is just the magnetic moment of a single electron because all but one of the electrons are paired. Because of the Pauli-exclusion principle, paired electrons (same non-spin quantum numbers) cannot have the same exact spin. As a result, no net magnetic moment is contributed by them. However, as a lone electron in the 5s shell, it is not paired and therefore can contribute the only measurable electron spin to the silver atom. So, silver atom only has the magnetic moment of just one electron.
### 1.4.c. Isotopes
**There are two different stable isotopes of silver (107 and 109) Would the two isotopes have produced different deflections on the photographic plate?**

Mass is not featured in the final equation for magnetic moment, so an isotope wouldn't add anything new.
### 1.4.d. Electrons
**Most people recall the Stern-Gerlach experiment involves the "spin of electron" and forget about the neutral silver atom. Could Stern and Gerlach have performed their experiment with a free electron traversing their magnet?**

The fact that the magnetic field sways the electron due to Lorentz force might make the experiment harder to measure, but spin is still spin. You would just see the picture to the right or left depending on how the magnetic field is oriented. Maybe a little warped too since the electrons actually experience the angled inhomogeneity of the magnetic field. 
### 1.4.e. g-factor
**The best measurement of the g-factor for the electron is somewhere around -2, usually quoted as the deviation from the normal Stern-Gerlach value of actually -2. How close is your photograph reading to the actual value?**

Just plug and chug:
> $\mu=geS/2m$; e is charge, m is mass, S is angular spin momentum
> $g=2m\mu/es$
> $=4m\mu/e\hbar$
> $=-1.8557$, close enough to $-2$...
## 1.5. Qubits???

> $\ket{\uparrow}=\ket{0}\to\begin{pmatrix}1 \\ 0\end{pmatrix}$
> $\ket{\uparrow}=\ket{1}\to\begin{pmatrix}0 \\ 1\end{pmatrix}$
> $M_H=\frac{1}{\sqrt{2}}\begin{pmatrix}1 & 1 \\ 1 & -1\end{pmatrix}$

a. Write $M_H$ as a linear combination of $\sigma$ and $I$.
> $M_H=\frac{1}{\sqrt{2}}\begin{pmatrix}1 & 1 \\ 1 & -1\end{pmatrix}=\frac{1}{\sqrt{2}}\begin{pmatrix}b+a_z & a_x-ia_y \\ a_x+ia_y & b-a_z\end{pmatrix}=\frac{1}{\sqrt{2}}(\vec{a}\cdot\vec{\sigma}+bI)$
> $\begin{pmatrix}0 & 0 & 1 & 1 & 1 \\ 1 & -i & 0 & 0 & 1 \\ 1 & i & 0 & 0 & 1 \\ 0 & 0 & -1 & 1 & -1\end{pmatrix}$
> $\begin{pmatrix}0 & 0 & 1 & 1 & 1 \\ 1 & -i & 0 & 0 & 1 \\ 2 & 0 & 0 & 0 & 2 \\ 0 & 0 & 0 & 2 & 0\end{pmatrix}$
> $\begin{pmatrix}0 & 0 & 1 & 0 & 1 \\ 0 & 1 & 0 & 0 & 0 \\ 1 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 1 & 0\end{pmatrix}$
> $a_x=1,a_y=0,a_z=1,b=0$

It's also not unreasonable to see that it's just an addition of the $\sigma_x$ and $\sigma_z$ matrices.
> $M_H=\frac{1}{\sqrt{2}}(\sigma_x+\sigma_z)$
> $M_H\ket{\uparrow}=\frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ 1\end{pmatrix}$
> $M_H\ket{\downarrow}=\frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ -1\end{pmatrix}$

This is useful in quantum computing because it introduces uncertainty into a known state, allowing for manipulation with this uncertainty as seen in Grover's algorithm. (The uncertain angle is manipulated such that it approaches the "right answer").

b. Find determinant and inverse of $M_H$
> $\det M_H=ac-bd=-2-2=-4$

Because the determinant isn't 0, an inverse is possible and easy since it's a 2x2:
> $M_H^{-1}=\frac{1}{\det M}\begin{pmatrix}d & -b \\ -c & a\end{pmatrix}=\frac{-1}{4}\begin{pmatrix}1 & -1 \\ 1 & 1\end{pmatrix}$

c. Suppose the following:
> $\ket{\psi}=\frac{3}{\sqrt{34}}\ket{\uparrow}+i\frac{5}{34}\ket{\downarrow}=\begin{pmatrix}\frac{3}{\sqrt{34}} \\ i\frac{5}{\sqrt{34}}\end{pmatrix}$

c.i. $|\braket{\uparrow|\psi}|^2$
> $=|\begin{pmatrix}1 & 0\end{pmatrix}\begin{pmatrix}\frac{3}{\sqrt{34}} \\ i\frac{5}{\sqrt{34}}\end{pmatrix}|^2$
> $=(\frac{3}{\sqrt{34}})^2$
> $=\frac{9}{34}$

c.ii. $\bra{\psi}S_x\ket{\psi}$
> $=\frac{\hbar}{2}\begin{pmatrix}\frac{3}{\sqrt{34}} & -i\frac{5}{\sqrt{34}}\end{pmatrix}\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}\begin{pmatrix}\frac{3}{\sqrt{34}} \\ i\frac{5}{\sqrt{34}}\end{pmatrix}$
> $=\frac{\hbar}{2}\begin{pmatrix}\frac{3}{\sqrt{34}} & -i\frac{5}{\sqrt{34}}\end{pmatrix}\begin{pmatrix}i\frac{5}{\sqrt{34}} \\ \frac{3}{\sqrt{34}}\end{pmatrix}$
> $=i\frac{\hbar}{2}\frac{15-15}{34}=0$

c.iii. $S_x\to-\frac{\hbar}{2}$
> The eigenvector corresponding to the eigenvalue $-1$ for the $\sigma_x$ measurement is what the eigenstate currently is given the qubit basis matrices:
> $\vec{v}_{-1,x}=\frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ -1\end{pmatrix}$
> The possible results of the $S_z$ measurements are the eigenstates it represents, which happen to obviously be the up and down qubit states. So now, let's find the probability using the Born rule with the eigenstates of the Z-measurement and the updated state.
> $\braket{\uparrow\mid\psi}^2=(\frac{1}{\sqrt{2}})^2=\frac{1}{2}$
> $\braket{\downarrow\mid\psi}^2=(-\frac{1}{\sqrt{2}})^2=\frac{1}{2}$

