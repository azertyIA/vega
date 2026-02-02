A *coherent state* is an eigenstate of the annihilation operator $\hat a$. But how is that possible? The annihilation operator isn't Hermitian. In general, one would thusly expect complex eigenvalues: $\alpha\in\mathbb{C}$.
> $\hat a\ket\Psi=\alpha\ket\Psi$
> $\hat a\ket\alpha=\alpha\ket\alpha$ (it's just a label)

Is this even a physical state? It has to be some combination of the Fock state SOBs.
> $\ket\alpha=\Sigma c_m\ket m,c_m\in\mathbb C$
> $\hat a\ket\alpha=\hat a\Sigma c_m\ket m,c_m\in\mathbb C$
> $=\Sigma c_m\hat a\ket m$
> $=\Sigma_{m=1}c_m\sqrt m\ket{m-1}$
> $=c_1\sqrt1\ket0+c_2\sqrt2\ket1+\dots$

But let's take the eigen value route:
> $\hat a\ket\alpha=\alpha\Sigma c_m\ket m,c_m\in\mathbb C$
> $=c_0\alpha\ket0+c_1\alpha\ket1+\dots$

So, we have a recursive thing:
> $c_{n}=\alpha c_{n-1}/\sqrt n$
> $c_{n}=\alpha^nc_0/\sqrt {n!}$

Putting it all together:
$$\ket\alpha=c_0\Sigma \alpha^m\ket m/\sqrt{m!}$$

And its dual to find the norm:
> $\bra\alpha=c_0^*\Sigma \alpha^{*m}\bra m/\sqrt{m!}$
> $\braket{\alpha|\alpha}=|c_0|^2\Sigma|a|^{2m}/m!=1$
> $=|c_0|^2e^{|a|^2}$

So $c_0$ should be normalized to:
> $c_0=e^{-|\alpha|^2/2}$
> $\ket\alpha=e^{-|\alpha|^2/2}\Sigma \alpha^m\ket m/\sqrt{m!}$
> $\bra\alpha=e^{-|\alpha|^2/2}\Sigma \alpha^{*m}\bra m/\sqrt{m!}$

We can do a little experiment on this:
> $\braket{\hat N}_\alpha=\braket{\alpha|a^\dagger a|\alpha}=|\alpha|^2$
> $\braket{\hat N^2}_\alpha=\braket{\alpha|a^\dagger aa^\dagger a|\alpha}$
> $=|\alpha|^2\braket{\alpha|aa^\dagger|\alpha}$
> $=|\alpha|^2\braket{\alpha|(1+a^\dagger a)|\alpha}$
> $=|\alpha|^2\bra{\alpha}(\ket{\alpha}+a^\dagger a\ket{\alpha})$
> $=|\alpha|^2(\bra{\alpha}\ket{\alpha}+\bra{\alpha}a^\dagger a\ket{\alpha})$
> $=|\alpha|^2(1+|\alpha|^2)$
> $\Delta N=\sqrt{|\alpha|^2}=|\alpha|$

For a specific Fock state:
> $P_m=|\braket{m|\alpha}|^2$
> $=e^{-|\alpha|^2}(|\alpha|^{2m})/m!$

One coherent state is an entire Hilbert Hotel. Or a nasty roach motel I guess.
> $\hat X=\hat x/\Delta_x$
> $\hat P=\hat p/\Delta_p$
> $\hat x=\Delta_x( a^\dagger+a)$
> $\hat p=i\Delta_x( a^\dagger-a)$

Applying these to the coherent states:
> $\bra{\alpha}\hat x\ket{\alpha}$
> $=\bra{\alpha}\Delta_x( a^\dagger+a)\ket{\alpha}$
> $=\Delta_x\bra{\alpha}( a^\dagger+a)\ket{\alpha}$
> $=\Delta_x(\bra{\alpha}a^\dagger\ket\alpha+\bra\alpha a\ket{\alpha})$
> $=\Delta_x(\alpha^*+\alpha)$
> $=2\Delta_x\mathfrak{Re}[\alpha]$
> $=2\Delta_p\mathfrak{Im}[\alpha]$

What about the variance and stuff?
> $\braket{x^2}_\alpha=\Delta_x^2\bra\alpha(aa+a^*a+aa^*+a^*a^*)\ket\alpha$
> $=(\alpha^2+\alpha^{*2})\Delta_x^2+\Delta_x^2\bra\alpha(1+2a^*a)\ket\alpha$
> $=(-1+\alpha^2+\alpha^{*2}+2|\alpha|^2)\Delta_x^2$
> $=((\alpha+\alpha^{*})^2-1)\Delta_x^2$
> $\Delta_x=\Delta x=\sqrt{\braket{x}^2-\braket{x^2}}$
> $\Delta_p=\Delta p=\sqrt{\braket{p}^2-\braket{p^2}}$

Let's put this on some ball, a fuzzy one with $\alpha=re^{i\theta}$, the time evolution would be:
> $\ket\alpha=e^{-|\alpha|^2/2}\Sigma \alpha^n\ket n/\sqrt{n!}$
> $\hat U(t,t_0)=e^{-i\hat H_0t/\hbar}$
> $\ket{\alpha,t}=e^{-i\hat H_0t/\hbar}e^{-|\alpha|^2/2}\Sigma \alpha^n\ket n/\sqrt{n!}$
> $\ket{\alpha,t}=e^{-|\alpha|^2/2}\Sigma \alpha^ne^{-i\hat H_0t/\hbar}\ket n/\sqrt{n!}$
> $\ket{\alpha,t}=e^{-|\alpha|^2/2}\Sigma \alpha^ne^{-i(n+1/2)\omega t}\ket n/\sqrt{n!}$
> $\ket{\alpha,t}=e^{-|\alpha|^2/2}\Sigma \alpha^ne^{-in\omega t}\ket n/\sqrt{n!}$ (the common phase was $\omega t/2$)
> $\ket{\alpha,t}=e^{-|\alpha e^{-i\omega t}|^2/2}\Sigma \alpha^ne^{-in\omega t}\ket n/\sqrt{n!}$ (exponential modulus = 1)
> $\ket{\alpha,t}=e^{-|\alpha e^{-i\omega t}|^2/2}\Sigma (\alpha e^{-i\omega t})^n\ket n/\sqrt{n!}$ 
> $\ket{\alpha,t}=\ket{\alpha e^{-i\omega t}}$ (label replacement, clockwise)

These coherent states are actually overcomplete SNOBS:
> $\frac1\pi\int d^2\alpha\ket\alpha\bra\alpha=I$
> There's nothing you can do to reduce it to $\aleph_1$

However they are NOT orthonormal:
> The kets will match up with the bras. There are infinite of each. Duh...

You can get to the ground state using a superconducting environment at $15$ mK.
> $k_BT=25$ meV, so if your $\hbar\omega$ is big enough, then you can get even room temperature stuff.

How do you actually make coherent states? You could try using the displacement operator.
> $\hat X=e^{-i\hat p\cdot b_1/\hbar}$
> $\hat P=e^{-i\hat x\cdot b_2/\hbar}$

So the claim is that you can just do some displacement across both fields using annihilation and creation with coefficients coming from $\alpha$.
> $e^{\hat A}\hat Be^{-\hat A}=\hat B+[\hat A,\hat B]+\frac12[\hat A,[\hat A,\hat B]]+\dots$
> $[\hat A,f(\hat B)]=[\hat A,\hat B]f'(\hat B)$
> $\hat D(\alpha)=e^{\alpha\hat a^\dagger-\alpha^*\hat a}$

> $f(\xi)=e^{\xi\hat A}e^{\xi\hat B}$
> $f'(\xi)=\hat Ae^{\xi\hat A}e^{\xi\hat B}+e^{\xi\hat A}\hat Be^{\xi\hat B}$
> $=\hat Ae^{\xi\hat A}e^{\xi\hat B}+e^{\xi\hat A}\hat Be^{\xi\hat B}$
> $=\hat Ae^{\xi\hat A}e^{\xi\hat B}+e^{\xi\hat A}\hat Be^{-\xi\hat A}e^{\xi\hat A}e^{\xi\hat B}$
> $=\hat Ae^{\xi\hat A}e^{\xi\hat B}+(\hat B+\xi[\hat A,\hat B])e^{\xi\hat A}e^{\xi\hat B}$
> $=(\hat A+\hat B+\xi[\hat A,\hat B])e^{\xi\hat A}e^{\xi\hat B}$
> $df/d\xi=(\hat A+\hat B+\xi[\hat A,\hat B])f$
> $df/f=d\xi(\hat A+\hat B+\xi[\hat A,\hat B])$
> $f=e^{\xi(\hat A+\hat B+\xi/2[\hat A,\hat B])}$
> $f(1)=e^{\hat A}e^{\hat B}=e^{\hat A+\hat B}e^{[\hat A,\hat B]/2}$
> $e^{\hat A}e^{\hat B}e^{-[\hat A,\hat B]/2}=e^{\hat A+\hat B}$

Applying it:
> $\hat D(\alpha)=e^{-|\alpha|^2/2}e^{\alpha\hat a^\dagger}e^{-\alpha^*\hat a}$
> $\Re(\alpha)=\braket{\hat x}/2m$
> $\Im(\alpha)=\braket{\hat p}/2m$
> $\hat D(\alpha)\ket0=e^{-|\alpha|^2/2}e^{\alpha\hat a^\dagger}e^{-\alpha^*\hat a}\ket0$
> $=e^{-|\alpha|^2/2}e^{\alpha\hat a^\dagger}({1-\alpha^*\hat a}+\dots)\ket0$
> $=e^{-|\alpha|^2/2}e^{\alpha\hat a^\dagger}\ket0$
> $=e^{-|\alpha|^2/2}(1+\alpha\hat a^\dagger+\frac12(\alpha\hat a^\dagger)^2+\dots)\ket0$
> $=e^{-|\alpha|^2/2}(\ket0+\alpha\sqrt1\ket1+\frac12\alpha^2\sqrt{1\cdot2}\ket2+\dots)$
> $=e^{-|\alpha|^2/2}\Sigma\frac{\alpha^n}{\sqrt{n!}}\ket n$
> $\Delta x\Delta p=1$
> $\braket{\hat N}_\alpha=|\alpha|^2$

You can also squeeze the balls to get a certain uncertainty in one direction, but does it also apply to phase angle and photon number? Kind of.

The LIGO has a wavelength of 1064 nm so about an energy of 1 eV. 