The [[Transmission Lines]] circuits go from $z=0\to l$
> $V(z)=v_+e^{-\gamma z}+v_-e^{+\gamma z}$
> $I(z)=i_+e^{-\gamma z}+i_-e^{+\gamma z}$

> $V(l)=v_+e^{-\gamma l}+v_-e^{+\gamma l}$
> $I(l)=v_+e^{-\gamma l}/Z_0-v_-e^{+\gamma l}/Z_0$

> $v_+=\frac12(V_L+I_LZ_0)e^{+\gamma l}$
> $v_-=\frac12(V_L-I_LZ_0)e^{-\gamma l}$

> $V(z)=\frac12I_L[(Z_L+Z_0)e^{+\gamma (l-z)}+(Z_L-Z_0)e^{-\gamma (l-z)}]$
> $I(z)=\frac12I_L/Z_0[(Z_L+Z_0)e^{+\gamma (l-z)}+(Z_L-Z_0)e^{-\gamma (l-z)}]$

Notice the $(l-z)$ and the sum terms. Set $z'$ to be the distance from the end. The quotient looks like a reflection coefficient.
> $V(z)=\frac12I_L[(Z_L+Z_0)e^{+\gamma z'}+(Z_L-Z_0)e^{-\gamma z'}]$
> $=\frac12I_L(Z_L+Z_0)[e^{+\gamma z'}+(Z_L-Z_0)/(Z_L+Z_0)e^{-\gamma z'}]$
> $=\frac12I_L(Z_L+Z_0)[e^{+\gamma z'}+\Gamma_Le^{-\gamma z'}]$

> $Z(z')=Z_0(1+\Gamma_Le^{-2\gamma z'})/(1-\Gamma_Le^{-2\gamma z'})$

At the source: 
> $Z_i=Z(z'=l)=Z_0(1+\Gamma_Le^{-2\gamma l})/(1-\Gamma_Le^{-2\gamma l})$

Now we have $V_g$ instead of $V_s$ (generator).
> $V_i=\frac{Z_i}{Z_i+Z_g}V_g$

Now, when we try to model out this shit, we usually assume the lossless case solely because we should be making very close to ideal transmission lines. We did it with op-amps too. Lossless is very achievable. Even so, you could approximate it to the first order and be fine. From here we will construct the Smith chart.
## Lossless TLs

Given the constants:
> $\gamma=\sqrt{(R+j\omega L)(G+j\omega C)}$
> $=j\omega\sqrt{LC}=jk$
> $k=\omega\sqrt{LC}$
> $v_{ph}=\omega/k=1/\sqrt{LC}$
> $Z_0=(R+j\omega L)/\gamma$
> $=j\omega L/j\omega\sqrt{LC}$
> $=\sqrt{L/C}+j0$

The ratio of $V_-/V_+=\Gamma_L$ or the amount that reflects compared to how much is incident.
> $V(z)=V_-e^{+jkz}+V_+e^{-jkz}$
> $=(V_+e^{-jkz})(1+\Gamma_Le^{+2jkz})$
> $=|V_+||e^{-jkz}||1+\Gamma_Le^{+2jkz}|$
> $=|V_+||1+\Gamma_Le^{+2jkz}|$
> $=|V_+|\sqrt{(1+\Gamma_Le^{+2jkz})(1+\Gamma_L^*e^{-2jkz})}$
> $=|V_+|\sqrt{1+2\Gamma_L\cos(2kz)+\Gamma_L^2}$
> $=|V_+|(1+\Gamma_L)$

We now have a incident wave and a reflected wave, which now creates a standing wave with hella nodes.
> $S=(1+|\Gamma_L|)/(1-|\Gamma_L|)$ (standing wave ratio)
> $S\in[1,\infty)$, (no reflection vs complete reflections)

Looking at this, we have 
> $Z_i=Z(z'=l)=Z_0(1+\Gamma_Le^{-j(\theta_r-2\gamma l)})/(1-\Gamma_Le^{-j(\theta_r-2\gamma l)})$
> $Z=Z(z'=0)=Z_0(1+\Gamma_Le^{-j\theta_r})/(1-\Gamma_Le^{-j\theta_r})$

They are off by a phase $2\gamma l$ or wave number multiplied by length.
## Smith Chart

![[Pasted image 20251112103651.png]]

> "This is the most difficult thing to get in Electrical Engineering" - Zach Star

The smith chart is constructed by starting off with a unit circle. What does it measure? The reflection coefficient. It can't go past a magnitude of 1, so you can capture the whole thing with a unit circle which has a length one. You have r-circles and x-circles.

For lossless:
> $Z_0=\sqrt{L/C}$

We have defined $\Gamma_L$ as such:
> $\Gamma_L=(Z_L-Z_0)/(Z_L+Z_0)$
> $=(R_L+jX_L-R_0)/(R_L+jX_L+R_0)$
> $=(R_L/R_0+jX_L/R_0-1)/(R_L/R_0+jX_L/R_0+1)$
> $=(r+jX_L/R_0-1)/(r+jX_L/R_0+1)$ ($r$ is normalized load resistance)
> $=(r+jx-1)/(r+jx+1)$ ($x$ is normalized load reactance)
> $=(\bar z_L-1)/(\bar z_L+1)$ (new definition? $\bar z_L=r+jx$)

To rewrite in terms of $\Gamma_L$:
> $\bar z_L\Gamma_L+\Gamma_L=\bar z_L-1$
> $\bar z_L(\Gamma_L-1)=-\Gamma_L-1$
> $\bar z_L(1-\Gamma_L)=1+\Gamma_L$
> $\bar z_L=r+jx=(1+\Gamma_L)/(1-\Gamma_L)$
> $\bar z_L=r+jx=(1+\Gamma_r+j\Gamma_i)/(1-\Gamma_r-j\Gamma_i)$

Now we have two different equations.
> $r+jx=(1+\Gamma_r+j\Gamma_i)(1-\Gamma_r+j\Gamma_i)/(1-\Gamma_r-j\Gamma_i)(1-\Gamma_r+j\Gamma_i)$
> $=(1+\Gamma_r+j\Gamma_i)(1-\Gamma_r+j\Gamma_i)/((1-\Gamma_r)^2+\Gamma_i^2)$

The numerator:
> $(1(1-\Gamma_r+j\Gamma_i)+\Gamma_r(1-\Gamma_r+j\Gamma_i)+j\Gamma_i(1-\Gamma_r+j\Gamma_i))$
> $=(1-\Gamma_r+j\Gamma_i)+(\Gamma_r-\Gamma_r^2+j\Gamma_i\Gamma_r)+(j\Gamma_i-j\Gamma_r\Gamma_i+j\Gamma_ij\Gamma_i)$
> $=(1+j\Gamma_i)+(-\Gamma_r^2)+(j\Gamma_i+\Gamma_i^2)$
> $=(1-(\Gamma_i^2+\Gamma_r^2))+j(2\Gamma_i)$

And now the result:
> $=(1-(\Gamma_i^2+\Gamma_r^2)+j(2\Gamma_i))/((1-\Gamma_r)^2+\Gamma_i^2)$
> $x=(1-\Gamma_i^2-\Gamma_r^2)/((1-\Gamma_r)^2+\Gamma_i^2)$
> $r=2\Gamma_i/((1-\Gamma_r)^2+\Gamma_i^2)$

You now can get two different families of circles:
> $[\Gamma_r-r/(1+r)]^2+[\Gamma_i]^2=[1/(1+r)]^2$
> $[\Gamma_r-1]^2+[\Gamma_i-1/x]^2=[1/x]^2$

**r-centers**: $(r/1+r,0)$, r-radii: $1/1+r$
- For $r=0$, you get a unit circle or a short circuit.
	- In between, you get a circle touching the imaginary axis.
- For $r=1$, you get resistance matching.
	- In between, you get a circle not touching the imaginary axis.
- For $r=\infty$, you get a point on or an open circuit.

**x-centers**: $(1,1/x)$, x-radii: $1/|x|$ (flipped for negative side)
- For $x=0$, you get the x-axis or a short circuit.
	- In between, you get a circle touching the imaginary axis.
- For $x=1$, you get a circle coinciding with the top.
	- In between, you get a circle not touching the imaginary axis.
- For $x=\infty$, you get the open circuit point.

Going back to this statement:
> They are off by a phase $2\gamma l$ or wave number multiplied by length.
> $2\gamma l=2\pi$ (on maximum)
> $l/\lambda=0.5$ (on maximum)

Do keep in mind that this stuff is still in terms of $\Gamma$ on the rectangular coordinate system.
> $\Gamma=|\Gamma|e^{j\phi}$

In short circuit, $r=0$, $x=0$, the phase angle is a pure $\pm\pi$.

Going back to this:
> $Z_i=Z(z'=l)=Z_0(1+\Gamma_Le^{-j(\theta_r-2\gamma l)})/(1-\Gamma_Le^{-j(\theta_r-2\gamma l)})$
> $Z_L=Z(z'=0)=Z_0(1+\Gamma_Le^{-j\theta_r})/(1-\Gamma_Le^{-j\theta_r})$

If $\Gamma_S$ is represented by point $P$, then you can draw a radius with $OP$ centered at the origin to get the circle where everything is the same magnitude. They split the main unit circle into four different constants based off the $2\gamma l$ thing.

Starting at short circuit, you go clockwise around until a ratio of one half to get the wavelength towards the generator. Go counter-clockwise to get the wavelength towards the load.

Let's just bring this back real quick:
> $S=(1+|\Gamma_L|)/(1-|\Gamma_L|)$ (standing wave ratio)
> $S\in[1,\infty)$, (no reflection vs complete reflections)
> We need to use some log scale (decibels) to plot this usefully.
> We also really hate it when signals bounce back, so lower is better.

For a special case: $l/\lambda=n/2$ or equivalently $2\gamma l=2\pi n$ for $n\in\mathbb{N}$:
> $z=r+j0$, $r<1$
> $\Gamma_L=\Gamma_r+j0<0$
> $\Gamma_L=1-2/(1+r)=(r-1)/(r+1)<0$
> $|\Gamma_L|=(1-r)/(r+1)$
> $S=((r+1)+(1-r))/((r+1)+(r-1))$ (standing wave ratio)
> $=2/2r=1/r$
