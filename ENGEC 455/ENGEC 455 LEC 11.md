Time averages are a lot more useful than instantaneous averages. 

Given a $\vec P$, the time average is:
> $\vec P_{avg}(\vec r)=\frac1T\int dt\vec P(\vec r,t)J$

But one useful thing about complex numbers at large is that:
> $c=a+jb$
> $2a=2\Re c=c+c^*$
> $2b=2\Im c=c-c^*$

Under an AC steady-state,
> $\vec P(\vec r,t)=\Re\vec[P(\vec r)e^{j\omega t}]$ (instantaneous (real) vs phasor form (imaginary))
> $\vec E(\vec r,t)\times\vec H(\vec r,t)=\Re[\vec E(\vec r,t)\times\vec H(\vec r,t)]$
> $=\Re[\vec E(\vec r,t)]\times\Re[\vec H(\vec r,t)]$
> $=\frac14((\vec E(\vec r)e^{j\omega t}+\vec E^*(\vec r)e^{-j\omega t})\times(\vec H(\vec r)e^{j\omega t}+\vec H^*(\vec r)e^{-j\omega t}))$
> $=\frac14((\vec E(\vec r)e^{j\omega t}\vec H(\vec r)e^{j\omega t}+\vec E^*(\vec r)e^{-j\omega t}\vec H(\vec r)e^{j\omega t}$
> $+\vec E(\vec r)e^{j\omega t}\vec H^*(\vec r)e^{-j\omega t}+\vec E^*(\vec r)e^{-j\omega t}\vec H^*(\vec r)e^{-j\omega t}))$
> $=\frac12(\Re[\vec E(\vec r)\times\vec H(\vec r)e^{2j\omega t}]+\Re[\vec E(\vec r)\times\vec H^*(\vec r)])$

And the average:
> $\vec P_{avg}(\vec r)=\frac1{2T}\int dt(\Re[\vec E(\vec r)\times\vec H(\vec r)e^{2j\omega t}]+\Re[\vec E(\vec r)\times\vec H^*(\vec r)])$
> $=\frac1{2T}\int dt(\Re[\vec E(\vec r)\times\vec H^*(\vec r)])$
> $=\frac12\Re[\vec E(\vec r)\times\vec H^*(\vec r)]$
> $=\frac12E_0H_0\hat k=\frac{E_0^2}{2\eta}\hat k=\frac{\eta H_0^2}{2}\hat k$

I wasted enough time.

There are two mediums, $(\mu_1,\epsilon_1,\eta_1)$ and $(\mu_2,\epsilon_2,\eta_2)$. Let's have a wave propagate from medium 1 to medium 2 dead on. If there was no difference between the two media then there would be no reflection. Otherwise there is transmission and reflection.
> $E_i=\hat xE_{i0}e^{-jkz};H_i=\hat yH_{i0}e^{-jkz}$
> $E_r=\hat xE_{r0}e^{+jkz};H_r=-\hat yH_{r0}e^{+jkz}$
> $E_t=\hat xE_{r0}e^{-jkz};H_t=\hat yH_{r0}e^{-jkz}$

