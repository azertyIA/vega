The electric field and the magnetic field each are related to each other via the Poynting vector:
> $\vec P=\vec E\times\vec H$

Imagine an incident wave coming to the right at a boundary x = 0. 
> ![[Pasted image 20251020103545.png]]

Two unknowns can only be solved with two independent equations. So we’re in a bit of trouble now, maybe? Faraday’s Law gives us the following:
> $\hat k\times\vec E=\eta\vec H$
> $\eta=\sqrt{\mu/\epsilon}$
> $H_0=E_0/\eta$
> $\eta_r=\eta_i\neq\eta_t$

What do we know about boundary conditions?
> $E_T=E_T$
> $H_T=H_T$
> $\epsilon E_N=\epsilon E_N$
> $\mu H_N=\mu H_N$

There are no normal fields in this problem, so all we know are that:
> $E_i+E_r=E_t$
> $H_i-H_r=H_t$
> $(E_i-E_r)/\eta_i=E_t/\eta_t$
> $\eta_t(E_i-E_r)/\eta_i=E_t$
> $\eta_t(E_i-E_r)/\eta_i=E_i+E_r$
> $\eta_tE_i-\eta_tE_r=\eta_iE_i+\eta_iE_r$
> $\eta_tE_i-\eta_iE_i-\eta_tE_r-\eta_iE_r=0$
> $E_i(\eta_t-\eta_i)-E_r(\eta_t+\eta_i)=0$
> $E_r=\frac\Delta\Sigma E_i=\Gamma E_i$
> $E_t=(1+\Gamma)E_i=\tau E_i$

What about the power?
> $\vec P_i=\hat k\frac{E^2_i}{2\eta}$
> $\vec P_r=-\hat k\frac{E^2_r}{2\eta}=-\hat k\Gamma^2\frac{E^2_i}{2\eta}$
> $\vec P_r=\hat k\frac{E^2_t}{2\eta}=-\hat k\tau^2\frac{E^2_i}{2\eta}$
> $\vec P_i=\vec P_r+\vec P_t$

In algebra, we used the summation of the complex and its conjugate to get the real component of the complex number. But apparently that doesn’t matter. If we have two materials of different permittivity and permeability, then we’re gonna see a difference in stuff.
> $(\mu_0,\epsilon_0,\eta_0)$ (air) vs $(\mu_0,\epsilon_w,\eta_w)$ (water)
> the scenario: $\epsilon_w>\epsilon_0$
> $\theta_i=\theta_c$ ($\theta_t=\pi/2$)

What about oblique incidence? 
> $\vec k=\hat xk_x+\hat zk_z$
> $\vec E_x=\hat zE_0e^{-jkx}$
> $\epsilon E_N=\epsilon E_N$
> $\mu H_N=\mu H_N$
> $\epsilon_1(E_i+E_r)=\epsilon_2E_t$