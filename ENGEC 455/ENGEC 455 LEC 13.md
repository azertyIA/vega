$Z_{in}=Z_0[Z_L+jZ_0\tan kl]$ (for lossless)

But for a small $kl$
$Z_{in}=Z_0[Z_L+jklZ_0]$ (for lossless)

$k=k_R+jk_I\to e^{k_Iz}e^{-jk_Rz}$

$V_0^-=\Gamma_LV_0^+$
$V(z)=V^+_0e^{-jkz}+V^-_0e^{+jkz}$
$=V^+_0e^{-jkz}+\Gamma_LV^+_0e^{+jkz}$
$=V^+_0[e^{-jkz}+\Gamma_Le^{+jkz}]$

(Case 1) $Z_L=0$, $\Gamma_L=(Z_L-Z_0)/(Z_L+Z_0)=-1$
> $V(z)=V^+_0[e^{-jkz}-e^{+jkz}]$
> $=-jV^+_0\sin kz$

(Case 2) $Z_L=\infty$, $\Gamma_L=(Z_L-Z_0)/(Z_L+Z_0)=1$
> $V(z)=V^+_0[e^{-jkz}+e^{+jkz}]$
> $=V^+_0\cos kz$

(Case 3) $Z_L=Z_0$, $\Gamma_L=(Z_L-Z_0)/(Z_L+Z_0)=0$
> $V(z)=V^+_0e^{-jkz}$

$$\boxed{\Gamma_L=(Z_L-Z_0)/(Z_L+Z_0)=\Gamma_r+j\Gamma_i}$$
For a lossless TL, $Z_0=\sqrt{L/C}>0$, but $Z_L=R_L+jX_L$

In smith charts, the unit circle for $r=0$ has the equation $\Gamma_r^2+\Gamma_i^2=1$. And this is just the normalized gamma. So if $|\Gamma|$ is its maximum at $1$, then the normalized resistance is $0$.

It should be really easy to find where a point should be, so just rotate that point to find the standing wave ratio (1/S or S depending on which side).

x-pos $=1-2/(1+r)=|\Gamma_L|$
$1+r=2/(1-|\Gamma_L|)$
$r=(1+|\Gamma_L|)/(1-|\Gamma_L|)=S$

OP is the magnitude/radius of the Smith chart. The difference between the phase angle between the load impedance and the input impedance is the $2kl$.

$Z$ is also $\eta$, so gamma can be written as such:
> $\Gamma=(\eta_L-\eta_0)/(\eta_L+\eta_0)$ where $\eta=\sqrt{\mu/\epsilon}=k*377(\Omega)$

## Plane of Incidence

The wave bounces and "rotates" about the xz plane, so the plane of incidence is such. No leak exists for total reflection. So the two waves are the ones that exist on that plane and the component that doesn't.

For a good conductor:
> $\epsilon_{eff}=\epsilon_0(1+\sigma/j\epsilon_0\omega)$
> $=\epsilon_0(\sigma/j\epsilon_0\omega)$
> $=(\sigma/j\omega)\to\infty$

> $\eta_1\to\infty$
> $\Gamma=\infty-\eta_0/\infty+\eta_0=1$
> $T=2\infty/\infty=2$

Yay I love Maxwell Equations:
> $\nabla\cdot\vec D=\rho$
> $\nabla\cdot\vec B=0$
> $\nabla\times\vec E=-\partial_t\vec H$
> $\nabla\times\vec H=\vec J_C+\partial_t\vec D$

The sources of an antenna are $\rho_V$ and $\vec J_C$. If they were not present, then,
> $\nabla\cdot\vec D=0$
> $\nabla\times\vec H=\partial_t\vec D$
> $(\nabla^2+\gamma^2+k^2)=0$
> $(\nabla^2+\gamma^2+k^2)\vec E=0$
> $\nabla(\nabla\cdot\vec E)-\nabla\times(\nabla\times\vec E)+(\gamma^2+k^2)\vec E=0$
> $-\nabla\times(\partial_t\vec H)+(\gamma^2+k^2)\vec E=0$
> $-\partial_t(\nabla\times\vec H)+(\gamma^2+k^2)\vec E=0$
> $-\partial_t(\partial_tD)+(\gamma^2+k^2)\vec E=0$
> $-\epsilon_0\partial_t^2\vec E+(\gamma^2+k^2)\vec E=0$
