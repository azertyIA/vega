# Homework 3
## 3.1. Sound Waves vs de Broglie Waves

a.i. T = 0.2 s
> $\omega=\frac{2\pi\text{ rad}}{T}=10\pi\text{ rad/s}$

a.ii. $\lambda=14\text{ m}$

a.iii. $v=\lambda/T=14/0.2=70 \text{ m/s}$

a.iv. Not enough information.

b.i. $\lambda=7*2=14\text{ nm}$

b.ii. $E=p^2/2m=\hbar^2k^2/2m$, $\lambda_C=2\pi\hbar/mc$
> $E/(mc^2)=\hbar^2k^2/2m^2c^2$
> $=4\pi^2\hbar^2/2m^2c^2\lambda^2$
> $=\lambda_C^2/2\lambda^2$
> $=(2.4*10^-3)/(28)$
> $=1.469*10^{-8}<<1$, which means non-relativistic

b.iii. $\nu/c=\omega/kc=\hbar\omega/c\hbar k$
> $=E/pc$
> $=p^2/2mpc$
> $=p/2mc$
> $=\hbar k/2mc$
> $=hc/\lambda2mc^2$
> $\approx1240/(14\cdot1.022*10^6)$
> $=8.67*10^{-5}$

b.iv. $\nu_g/c=hk/mc$
> $=2*8.67*10^{-5}$
> $=1.73*10^{-4}$

The group speed is double the magnitude of the phase speed. The speeds are nowhere near the speed of light, so everything is non relativistic.

b.v. Spatially, the cosine should lag behind the sine. So, quantifying this, the real part should be cosine and should be behind. However, the real part is actually ahead, signifying the sine wave is actually negative, or perhaps its inside is negative. Thus, the spatial wavenumber k should be negative or at least moving in the left direction.

c. Based on a still image you don't know what direction a sound wave is traveling unlike having both components of a still de Broglie wave. However they are the same in that they have a wave number and angular frequency. 
## 3.2. Commutators and Operators
### 3.2.a. Hadamard's Operator Lemma: 

Start with $e^ABe^{-A}$:
> $=(1+A+\frac{1}{2}A^2+\dots)B(1-A+\frac{1}{2}A^2+\dots)$
> $=(1+A+\frac{1}{2}A^2+\dots)B(1-A+\frac{1}{2}A^2+\dots)$
> $=(B+AB+\frac{1}{2}A^2B+\dots)(1-A+\frac{1}{2}A^2+\dots)$
> $=(B-BA+\frac{1}{2}BA^2+\dots)+(AB-ABA+\frac{1}{2}ABA^2+\dots)+\frac{1}{2}(A^2B-A^2BA+\frac{1}{2}A^2BA^2+\dots)$
> $=\Sigma_n\Sigma_m\frac{1}{n!m!}(-1)^{m}A^nBA^m$

What if we wanted to write the sum in terms of the $h=mO+n$ and $m$? We still hit every one.
> $=\Sigma_h\Sigma_m^h\frac{1}{(h-m)!m!}(-1)^{m}A^{(h-m)}BA^m$

Let's address the super-commutator:
> $[A,B]=AB-BA$
> $[A,AB-BA]=AAB-ABA-ABA+BAA$

In other words, a "super-commutator" produces all "positions" that represent placing As around a B, with total "A"s being the commutators taken. In a commutator, the part that puts the "A" on the right (physically) side of B is negative, so it makes sense that an odd number of A's to the right of B would result in a negative term: (duplicates are counted courtesy of Pascal's Triangle a.k.a. combinatoric)
> $[A,[A,\cdots]]=\Sigma_{m=0}^n(-1)^m\frac{n!}{m!(n-m)!}A^{n-m}BA^{m}$

You'll realize that this format closely resembles the grouping of different "degrees" of terms from the exponential side of the problem. Because they are the same.
> $=\Sigma_{h=0}\Sigma_{m=0}^h(-1)^m\frac{1}{m!(h-m)!}A^{h-m}BA^{m}$
> $=\Sigma_{h=0}\frac{1}{h!}\Sigma_{m=0}^h(-1)^m\frac{h!}{m!(h-m)!}A^{h-m}BA^{m}$
> $=\Sigma_{h=0}\frac{1}{h!}[A,A[\dots]]$

### 3.2.b. Unnamed Lemma
Start with $[\hat A,\hat B]f'(\hat B)$
> $\to f(\hat B)=\Sigma\frac{1}{n!}\hat B^nf^{(n)}(0)$
> $\to f'(\hat B)=\Sigma\frac{1}{(n-1)!}\hat B^{(n-1)}f^{(n)}(0)$
> $\to \hat Af(\hat B)=\Sigma\frac1{n!}\hat A\hat B^nf^{(n)}(0))$

We need to be better equipped for this: Let $f(m,n)=\hat B^m[\hat A,\hat B^n]$
> $\to f(m,0)=0$
> $\to f(m,1)=\hat B^m[\hat A,\hat B]$
> $\to f(m,n)=\hat B^m[\hat A,\hat B\hat B^{n-1}]$
> $=\hat B^{m+1}[\hat A,\hat B^{n-1}]+\hat B^{m+n-1}[\hat A,\hat B]$
> $=f(m+2,n-2)+2f(m+n-1,1)$
> $=f(m+n,n-n)+nf(m+n-1,1)$
> $=f(m+n,0)+nf(m+n-1,1)=nf(m+n-1,1)$

So this power ends up being true.
> $[\hat A,\hat B^n]=f(0,n)=n[\hat A,\hat B]B^{n-1}$

Meanwhile,
> $[\hat A,f(\hat B)]=[\hat A,\Sigma\frac1{n!}\hat B^nf^{(n)}(0)]$
> $=\Sigma\frac1{n!}[\hat A,\hat B^nf^{(n)}(0)]$
> $=\Sigma\frac1{n!}f^{(n)}(0)[\hat A,\hat B^n]$
> $=\Sigma\frac1{n!}f^{(n)}(0)n[\hat A,\hat B]B^{n-1}$
> $=[\hat A,\hat B]\Sigma\frac1{n!}f^{(n)}(0)nB^{n-1}$
> $=[\hat A,\hat B]\Sigma\frac1{(n-1)!}f^{(n)}(0)B^{n-1}$
> $=[\hat A,\hat B]f'(\hat B)$

Additionally, the converse should work the same: Let $f(m,n)=\hat A^m[\hat A^n,\hat B]$
> $\to f(m,0)=0$
> $\to f(m,1)=\hat A^m[\hat A,\hat B]$
> $\to f(m,n)=\hat A^m[\hat A\hat A^{n-1},\hat B]$
> $=\hat A^{m+1}[\hat A^{n-1},\hat B]+\hat A^{m+n-1}[\hat A,\hat B]$
> $=f(m+1,n-1)+f(m+n-1,1)$
> $=nf(m+n-1,1)$
> $[\hat A^n,\hat B]=f(0,n)=nf(n-1,1)=n\hat A^{n-1}[\hat A,\hat B]$

So rearranging and substituting:
> $[g(\hat A),\hat B]=\Sigma\frac1{n!}[\hat A^ng^{(n)}(0),\hat B]$
> $=\Sigma\frac1{n!}g^{(n)}(0)[\hat A^n,\hat B]$
> $=\Sigma\frac1{n!}g^{(n)}(0)n\hat A^{n-1}[\hat A,\hat B]$
> $=\Sigma\frac1{(n-1)!}g^{(n)}(0)\hat A^{n-1}[\hat A,\hat B]$
> $=g'(\hat A)[\hat A,\hat B]$
## 3.3. Eigen Eigen Eigen

Given:
> $H=\begin{pmatrix}\epsilon_0&\gamma e^{-i\chi}\\\gamma e^{+i\chi}&\epsilon_1\end{pmatrix}$

### 3.3.a. Eigenvalues

Find eigenvalues $\epsilon_g$ and $\epsilon_e$
> $\det (H-\lambda I)=0$
> $=(\epsilon_0-\lambda)(\epsilon_1-\lambda)-\gamma^2=0$
> $=\epsilon_0\epsilon_1-\lambda(\epsilon_0+\epsilon_1)+\lambda^2-\gamma^2$
> $=\lambda^2-\lambda(\epsilon_0+\epsilon_1)+\epsilon_0\epsilon_1-\gamma^2$
> $\to\lambda=(\epsilon_0+\epsilon_1\pm\sqrt{\epsilon_0^2+2\epsilon_0\epsilon_1+\epsilon_1^2-4\epsilon_0\epsilon_1+4\gamma^2})/2$
> $=(\epsilon_0+\epsilon_1\pm\sqrt{\epsilon_0^2-2\epsilon_0\epsilon_1+\epsilon_1^2+4\gamma^2})/2$
> $=(\epsilon_0+\epsilon_1\pm\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})/2$
> $\epsilon_g=(\epsilon_0+\epsilon_1+\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})/2$
> $\epsilon_e=(\epsilon_0+\epsilon_1-\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})/2$
 

### 3.3.b. Eigenvectors

Find their respective eigenvectors $\ket{\psi_g}$ and $\ket{\psi_e}$ 
Apply Axiom 1 and realize that given a wave vector $\begin{pmatrix}\alpha\\\beta\end{pmatrix}$:
> $|\alpha|^2+|\beta|^2=1$, any phase can be present as a coefficient.
> $\alpha=\cos\mu$
> $\beta=e^{i\phi}\sin\mu$

Now we try solving with the now constraints:
> $\epsilon_0\alpha_g+\gamma e^{-i\chi}\beta_g=\epsilon_g\alpha_g$
> $\to0=(\epsilon_0-\epsilon_g)\alpha_g+\gamma e^{-i\chi}\beta_g$
> $=(\epsilon_0-\epsilon_g)\cos\mu+\gamma e^{-i\chi}e^{i\phi}\sin\mu_g$
> $=(\epsilon_0-\epsilon_g)\cos\mu+\gamma e^{-i(\chi-\phi)}\sin\mu_g$

I'll be setting $\mu=\mu_g$ for now. There are no imaginary components featured anywhere else, so the exponential factor must be completely real ($\pm1$), but we'll assume it's 1 for now:
> $=(\epsilon_0-\epsilon_g)\cos\mu\pm\gamma\sin\mu$
> $\to\gamma\sin\mu=(\epsilon_g-\epsilon_0)\cos\mu$
> $\to\tan\mu=(\epsilon_g-\epsilon_0)/\gamma$

Now let's look at this identity
> $\tan2\mu=2\tan\mu/(1-\tan^2\mu)$
> $\tan2\mu=\frac{2(\epsilon_g-\epsilon_0)}{\gamma}/(1-\frac{(\epsilon_g-\epsilon_0)^2}{\gamma^2})$
> $\tan2\mu=\frac{2(\epsilon_g-\epsilon_0)}{\gamma}/\frac{\gamma^2-(\epsilon_g-\epsilon_0)^2}{\gamma^2}$
> $\tan2\mu=\frac{2(\epsilon_g-\epsilon_0)}{\gamma}\cdot\frac{\gamma^2}{\gamma^2-(\epsilon_g-\epsilon_0)^2}$
> $\tan2\mu=\frac{2(\epsilon_g-\epsilon_0)}{\gamma}\cdot\frac{\gamma^2}{(\epsilon_0-\epsilon_g)(\epsilon_1-\epsilon_g)-(\epsilon_g-\epsilon_0)^2}$, look at kernel
> $\tan2\mu=\frac{2(\epsilon_g-\epsilon_0)}{\gamma}\cdot\frac{\gamma^2}{(\epsilon_0-\epsilon_g)((\epsilon_1-\epsilon_g)-(\epsilon_0-\epsilon_g))}$
> $\tan2\mu=\frac{2(\epsilon_g-\epsilon_0)}{\gamma}\cdot\frac{\gamma^2}{(\epsilon_0-\epsilon_g)(\epsilon_1-\epsilon_0)}$
> $\tan2\mu=\frac{2}{1}\cdot\frac{\gamma}{\epsilon_0-\epsilon_1}$
> $\tan2\mu=\frac{2\gamma}{\epsilon_0-\epsilon_1}$

Now selecting an easy case where $\phi=\chi$, we have a good set of eigenvectors:
> $\ket{\psi_g}=\cos\mu_g\ket0+e^{+i\chi}\sin\mu_g\ket1$, $\tan2\mu_g=\frac{2\gamma}{\epsilon_0-\epsilon_1}$

For the other vector however, we would get the same result but with a $\mu_e$.
> $\ket{\psi_e}=\cos\mu_e\ket0+e^{+i\chi}\sin\mu_e\ket1$, $\tan2\mu_e=\frac{2\gamma}{\epsilon_0-\epsilon_1}$

However, we have the following condition:
> $\tan\mu_g=(\epsilon_g-\epsilon_0)/\gamma$
> $\tan\mu_e=(\epsilon_e-\epsilon_0)/\gamma$

Writing out the eigenvalues get bland very, very fast. So let's do it better:
> $\delta=\epsilon_0-\epsilon_1$
> $\sigma=\delta^2+4\gamma^2$

So time to substitute:
> $\epsilon-\epsilon_0=(-(\epsilon_0-\epsilon_1)\pm\sqrt{(\epsilon_0-\epsilon_1)^2+4\gamma^2})/2$
> $\epsilon-\epsilon_0=(-\delta\pm\sqrt\sigma)/2$

So, what's the two tangents multiplied together?
> $\tan\mu_g\tan\mu_e=(\epsilon_g-\epsilon_0)(\epsilon_e-\epsilon_0)/\gamma^2$
> $=((-\delta+\sqrt\sigma)/2)(-\delta-\sqrt\sigma)/2)/\gamma^2$
> $=(-\delta+\sqrt\sigma)(-\delta-\sqrt\sigma)/4\gamma^2$
> $=(\delta^2-\sigma)/4\gamma^2$
> $=-4\gamma^2/4\gamma^2$
> $=-1$
b. Find their respective eigenvectors $\ket{\psi_g}$ and $\ket{\psi_e}$

Then, we have a pretty useful product to relate the angles:
> $\tan\mu_g\tan\mu_e=-1$
> $\tan\mu_g=-\cot\mu_e=\cot(-\mu_e)=\tan(\frac\pi2+\mu_e)$
> $\mu_e=\mu_g-\frac\pi2$

Now substitute:
> $\ket{\psi_e}=\cos(\mu_g-\frac\pi2)\ket0+e^{+i\chi}\sin(\mu_g-\frac\pi2)\ket1$
> $\ket{\psi_e}=\sin\mu_g\ket0-e^{+i\chi}\cos\mu_g\ket1$
> $\ket{\psi_e}=-\sin\mu\ket0+e^{+i\chi}\cos\mu\ket1$, $\tan2\mu=\tan2\mu_g=\frac{2\gamma}{\epsilon_0-\epsilon_1}$

So now we're finally done with this part:
> $\tan2\mu=\tan2\mu_g=\frac{2\gamma}{\epsilon_0-\epsilon_1}$
> $\ket{\psi_g}=\cos\mu\ket0+e^{+i\chi}\sin\mu\ket1$
> $\ket{\psi_e}=-\sin\mu\ket0+e^{+i\chi}\cos\mu\ket1$
### 3.3.c. Time Evolution

Find the matrix representation of the time evolution operator:
> $U(t,t_0)=\ket{\psi_g}e^{-\frac i\hbar\epsilon_g(t-t_0)}\bra{\psi_g}+\ket{\psi_e}e^{-\frac i\hbar\epsilon_e(t-t_0)}\bra{\psi_e}$

Let's look at the first term:
> $=(\cos\mu\ket0+e^{+i\chi}\sin\mu\ket1)e^{-\frac i\hbar\epsilon_g(t-t_0)}(\cos\mu\bra0+e^{-i\chi}\sin\mu\bra1)$
> $=e^{-\frac i\hbar\epsilon_g(t-t_0)}(\cos\mu\ket0+e^{+i\chi}\sin\mu\ket1)(\cos\mu\bra0+e^{-i\chi}\sin\mu\bra1)$
> $=e^{-\frac i\hbar\epsilon_g(t-t_0)}(\cos\mu\ket0(\cos\mu\bra0+e^{-i\chi}\sin\mu\bra1)+e^{+i\chi}\sin\mu\ket1(\cos\mu\bra0+e^{-i\chi}\sin\mu\bra1))$
> $=e^{-\frac i\hbar\epsilon_g(t-t_0)}((\cos\mu\ket0\cos\mu\bra0+\cos\mu e^{-i\chi}\sin\mu\ket0\bra1)+e^{+i\chi}\sin\mu\ket1(\cos\mu\bra0+e^{-i\chi}\sin\mu\bra1))$
> $=e^{-\frac i\hbar\epsilon_g(t-t_0)}(\cos^2\mu\ket0\bra0+\cos\mu\sin\mu e^{-i\chi}\ket0\bra1+e^{+i\chi}\sin\mu\ket1(\cos\mu\bra0+e^{-i\chi}\sin\mu\bra1))$
> $=e^{-\frac i\hbar\epsilon_g(t-t_0)}(\cos^2\mu\ket0\bra0+e^{-i\chi}\cos\mu\sin\mu \ket0\bra1+e^{+i\chi}\sin\mu\cos\mu\ket1\bra0+\sin^2\mu\ket1\bra1)$

And repeat the logic for the second term:
> $=e^{-\frac i\hbar\epsilon_e(t-t_0)}(\sin^2\mu\ket0\bra0-e^{-i\chi}\cos\mu\sin\mu \ket0\bra1-e^{+i\chi}\sin\mu\cos\mu\ket1\bra0+\cos^2\mu\ket1\bra1)$

And combine:
> $\begin{pmatrix}\cos^2\mu&e^{-i\chi}\cos\mu\sin\mu\\e^{+i\chi}\cos\mu\sin\mu&\sin^2\mu\end{pmatrix}e^{-\frac i\hbar\epsilon_g(t-t_0)}+\begin{pmatrix}\sin^2\mu&-e^{-i\chi}\cos\mu\sin\mu\\-e^{+i\chi}\cos\mu\sin\mu&\cos^2\mu\end{pmatrix}e^{-\frac i\hbar\epsilon_e(t-t_0)}$

d. If $\chi$ were time-dependent, then the eigenvalues themselves wouldn't change, but everything else including the Hamiltonian, time-evolution operator and the eigenstates would change. The eigenstates in particular would have their ratios change in phase.
## 3.4. Heisenberg is Uncertain

a. Prove that $\braket{\alpha|\alpha}\braket{\beta|\beta}=\frac14|\braket{[\hat A,\hat B]}|^2$:
> $|\ket{\alpha}+\lambda\ket{\beta}|^2\geq0$ (all magnitudes should be positive)
> $(\bra\alpha+\lambda^*\bra\beta)(\ket\alpha+\lambda\ket\beta)\geq0$
> $(\braket{\alpha|\alpha}+\lambda^*\braket{\beta|\alpha}+\lambda\braket{\alpha|\beta}+|\lambda|^2\braket{\beta|\beta})\geq0$

Now assume $\lambda=-\braket{\beta|\alpha}/\braket{\beta|\beta}$
> $\lambda^*=-\braket{\alpha|\beta}/\braket{\beta|\beta}$
> $(\braket{\alpha|\alpha}-\braket{\alpha|\beta}\braket{\beta|\alpha}/\braket{\beta|\beta}-\braket{\beta|\alpha}\braket{\alpha|\beta}/\braket{\beta|\beta}+|\lambda|^2\braket{\beta|\beta})\geq0$
> $\braket{\alpha|\alpha}-2\braket{\beta|\alpha}\braket{\alpha|\beta}/\braket{\beta|\beta}+|\braket{\beta|\alpha}|^2/\braket{\beta|\beta}\geq0$
> $\braket{\alpha|\alpha}\braket{\beta|\beta}-\braket{\beta|\alpha}\braket{\alpha|\beta}\geq0$
> $\braket{\alpha|\alpha}\braket{\beta|\beta}\geq\braket{\beta|\alpha}\braket{\alpha|\beta}$
> $\braket{\alpha|\alpha}\braket{\beta|\beta}\geq|\braket{\alpha|\beta}|^2$

b. Prove that expectation values of Hermitian operators are purely real:
> $\hat H=\hat H^\dagger$ (Hermitian)
> $\bra\psi\hat H\ket\psi=(\bra\psi\hat H\ket\psi)^*=\bra\psi\hat H^\dagger\ket\psi$ (expectation value)
> $\braket H=\braket H^*$
> $\alpha+i\beta=\alpha-i\beta$ (decomposition)
> $2i\beta=0$, imaginary part is 0, there only exists the real component

c. Prove that expectation values of anti-Hermitian operators are purely imaginary:
> $\hat A=-\hat A^\dagger$ (anti-Hermitian)
> $\bra\psi\hat A\ket\psi=-(\bra\psi\hat A\ket\psi)^*=-\bra\psi\hat A^\dagger\ket\psi$ (expectation value)
> $\braket A=-\braket A^*$
> $\alpha+i\beta=-\alpha+i\beta$ (decomposition)
> $2\alpha=0$, real part is 0, there only exists the imaginary component

d. Prove that $\braket{\Delta\hat A\Delta\hat B}=\frac12\braket{[\hat A,\hat B]}+\frac12\braket{\{\Delta\hat A,\Delta\hat B\}}$:
> $[\Delta\hat A,\Delta\hat B]+\{\Delta\hat A,\Delta\hat B\}=2\Delta\hat A\Delta\hat B + 0$
> $\bra\psi[\Delta\hat A,\Delta\hat B]\ket\psi+\bra\psi\{\Delta\hat A,\Delta\hat B\}\ket\psi=2\bra\psi\Delta\hat A\Delta\hat B\ket\psi$
> $\braket{[\Delta\hat A,\Delta\hat B]}+\braket{\{\Delta\hat A,\Delta\hat B\}}=2\braket{\Delta\hat A\Delta\hat B}$

However, $[\Delta\hat A,\Delta\hat B]=[\hat A-\braket A,\hat B-\braket B]$, and the expected values are just scalars that will commute and cancel terms out such that $[\Delta\hat A,\Delta\hat B]=[\hat A,\hat B]$:
>$\braket{\Delta\hat A\Delta\hat B}=\frac12\braket{[\hat A,\hat B]}+\frac12\braket{\{\Delta\hat A,\Delta\hat B\}}$

To check how the components work, we can see if the commutator and anti-commutator are Hermitian or anti-Hermitian:
> $[\hat A,\hat B]^\dagger=\hat B\hat A-\hat A\hat B=-[\hat A,\hat B]$, commutator is anti-Hermitian
> $\{\hat A,\hat B\}^\dagger=\hat B\hat A+\hat A\hat B=\{\hat A,\hat B\}$, anti-commutator is Hermitian

In combination with lemmas from parts b and c, the commutator is the purely imaginary part while the anti-commutator is the purely real part.

e. Prove that $\braket{(\Delta\hat A)^2}\braket{(\Delta\hat B)^2}\geq\frac14|\braket{[\hat A,\hat B]}|^2$
> Assume $\ket\alpha=\Delta\hat A\ket\psi$ and $\ket\beta=\Delta\hat B\ket\psi$
> $\braket{\alpha|\alpha}\braket{\beta|\beta}\geq|\braket{\alpha|\beta}|^2$ (lemma from part a)
> $\bra\psi(\Delta\hat A)^2\ket\psi\bra\psi(\Delta\hat B)^2\ket\psi\geq|\bra\psi\Delta\hat A\Delta\hat B\ket\psi|^2$ (Hermitian)
> $\braket{(\Delta\hat A)^2}\braket{(\Delta\hat B)^2}\geq|\braket{\Delta\hat A\Delta\hat B}|^2$
> $\braket{(\Delta\hat A)^2}\braket{(\Delta\hat B)^2}\geq\frac14|\braket{[\hat A,\hat B]}+\braket{\{\Delta\hat A,\Delta\hat B\}}|^2$
> $\braket{(\Delta\hat A)^2}\braket{(\Delta\hat B)^2}\geq\frac14|\braket{[\hat A,\hat B]}|^2+\frac14|\braket{\{\Delta\hat A,\Delta\hat B\}}|^2$ (one is real the other imaginary)

This is true. However, since the last term is definitely positive:
> $\frac14|\braket{[\hat A,\hat B]}|^2+\frac14|\braket{\{\Delta\hat A,\Delta\hat B\}}|^2\geq\frac14|\braket{[\hat A,\hat B]}|^2$

Which means this is also true:
> $\braket{(\Delta\hat A)^2}\braket{(\Delta\hat B)^2}\geq\frac14|\braket{[\hat A,\hat B]}|^2$
## 3.5. Harmony and Superposition

### 3.5.a. Chutes and Ladders

Given:
> $\hat H\ket{\Psi_n,t=0}=E_n\ket{\Psi_n,t=0}=\hbar\omega_0(n+\frac12)c_n\ket n$
> $\ket{\Psi_n,t}=e^{-\frac i\hbar\hat Ht}\ket{\Psi_n,t=0}=e^{-\frac i\hbar E_nt}\ket{\Psi_n,t=0}$

The time dependent wave function must then be:
> $\ket{\Psi,t}=\frac1{\sqrt2}e^{-\frac i\hbar E_0t}\ket0+\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket1$
> This is already normalized.

Now adding the position parameter:
> $\braket{x|\Psi,t}=\Psi(x,t)=\frac1{\sqrt2}e^{-iE_0t/\hbar}\braket{x|0}+\frac{e^{i\delta}}{\sqrt2}e^{-iE_1t/\hbar}\braket{x|1}$
> $\braket{x|\Psi,t}=\Psi(x,t)=\frac1{\sqrt2}e^{-iE_0t/\hbar}\phi_0(x)+\frac{e^{i\delta}}{\sqrt2}e^{-iE_1t/\hbar}\phi_1(x)$

How would we go about solving the harmonic oscillator though?
> $\hat a=\sqrt{m\omega_0/2\hbar}(x+ip/m\omega_0)$ (annihilation)
> $\hat a^\dagger=\sqrt{m\omega_0/2\hbar}(x-ip/m\omega_0)$ (creation)
> $[\hat a,\hat a^\dagger]=1$
> $\hat N=\hat a^\dagger\hat a=(m\omega_0/2\hbar)(x^2+p^2/m^2\omega_0^2+i[x,p]/m\omega_0)$
> $=(1/2\hbar\omega_0)(m\omega_0^2x^2+p^2/m)-1/2$ (canonical commutator = $i\hbar$)
> $=\hat H/\hbar\omega_0-1/2$ 

This operator essentially takes the energy level and pastes it before the ket:
> $\hat N\ket n=n\ket n$

Applying $\hat a$, $\hat a^\dagger$, and $\hat N$ gets us the following: 
> $[\hat N,\hat a]=[\hat a^\dagger\hat a,\hat a]$
> $=\hat a^\dagger[\hat a,\hat a]+[\hat a^\dagger,\hat a]\hat a$
> $=0+(-1)\hat a=-\hat a$
> $[\hat N,\hat a^\dagger]=[\hat a^\dagger\hat a,\hat a^\dagger]$
> $=\hat a^\dagger[\hat a,\hat a^\dagger]+0=\hat a^\dagger$

So now let's see what they actually do to kets because the annihilation and creation operators do not preserve the state of the ket. So technically they probably shouldn't have hats as I have here.
> $\hat Na^\dagger\ket n=([\hat N,a^\dagger]+a^\dagger\hat N)\ket n$
> $=(a^\dagger I+a^\dagger\hat N)\ket n$
> $=a^\dagger (I+N)\ket n=(n+1)a^\dagger\ket n$

> $\hat Na\ket n=([\hat N,a]+a\hat N)\ket n$
> $=(-aI+a\hat N)\ket n$
> $=(n-1)a\ket n$

By that logic it's almost as if the annihilation operator changes the energy level of the ket down by one and the creation operator up by one. But it has to be off by some normalization coefficient.
> $a\ket n=c\ket{n-1}$
> $\bra na^\dagger a\ket n=\bra n\hat N\ket n=n\braket{n|n}=n=|c|^2$
> $a^\dagger\ket n=c\ket{n+1}$
> $\bra naa^\dagger\ket n=\bra n([a,\hat a]+\hat N)\ket n=\bra n(1+\hat N)\ket n=n+1=|c|^2$

In position space, the x operator is just $x$ while the momentum operator is $-i\hbar\partial_x$
> $\hat a=\sqrt{m\omega_0/2\hbar}(x+\frac{\hbar}{m\omega_0}\frac d{dx})$ (annihilation)

Applying to the lowest eigenstate:
> $\hat a\braket{x|0}=\hat a\phi_0(x)=0$
> $=(x+\frac{\hbar}{m\omega_0}\frac d{dx})\phi_0=0$ 
> $\to x\phi_0=-\frac{\hbar}{m\omega_0}\frac{d\phi_0}{dx}$ 
> $\to -\frac{m\omega_0}\hbar x dx=\frac{d\phi_0}{\phi_0}$ 
> $\to -\frac{m\omega_0}{2\hbar} x^2+C=\ln\phi_0$ 
> $\to\phi_0(x)=C\exp(-\frac{m\omega_0}{2\hbar} x^2)$

Repeating a similar but exhausting process found in the textbook yields the next energy eigenstate, so now the function is better defined:
> $\phi_0(x)=(\frac{m\omega_0}{\pi\hbar})^{1/4}e^{-m\omega_0x^2/2\hbar}$
> $\phi_1(x)=(\frac{m\omega_0}{\pi\hbar})^{1/4}\sqrt{\frac{2m\omega_0}\hbar}xe^{-m\omega_0x^2/2\hbar}$
> $\braket{x|\Psi,t}=\Psi(x,t)=\frac1{\sqrt2}e^{-iE_0t/\hbar}\phi_0(x)+\frac{e^{i\delta}}{\sqrt2}e^{-iE_1t/\hbar}\phi_1(x)$

### 3.5.b. Hamiltonian
$\bra{\Psi,t}\hat H\ket{\Psi,t}$
> $=(\frac1{\sqrt2}e^{-\frac i\hbar E_0t}\ket0+\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket1)^*\hat H(\frac1{\sqrt2}e^{-\frac i\hbar E_0t}\ket0+\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket1)$
> $=\frac12(e^{\frac i\hbar E_0t}\bra0+e^{-i\delta}e^{\frac i\hbar E_1t}\bra1)(e^{-\frac i\hbar E_0t}\hat H\ket0+e^{i\delta}e^{-\frac i\hbar E_1t}\hat H\ket1)$
> $=\frac14\hbar\omega_0(e^{\frac i\hbar E_0t}\bra0+e^{-i\delta}e^{\frac i\hbar E_1t}\bra1)(e^{-\frac i\hbar E_0t}\ket0+3e^{i\delta}e^{-\frac i\hbar E_1t}\ket1)$
> $=\frac14\hbar\omega_0(e^{\frac i\hbar E_0t}\bra0(e^{-\frac i\hbar E_0t}\ket0+3e^{i\delta}e^{-\frac i\hbar E_1t}\ket1)+e^{-i\delta}e^{\frac i\hbar E_1t}\bra1(e^{-\frac i\hbar E_0t}\ket0+3e^{i\delta}e^{-\frac i\hbar E_1t}\ket1))$
> $=\frac14\hbar\omega_0(\bra0\ket0+3e^{\frac i\hbar E_0t}\bra0e^{i\delta}e^{-\frac i\hbar E_1t}\ket1+e^{-i\delta}e^{\frac i\hbar E_1t}\bra1e^{-\frac i\hbar E_0t}\ket0+3\bra1\ket1)$
> $=\frac14\hbar\omega_0(1+3e^{\frac i\hbar E_0t}e^{i\delta}e^{-\frac i\hbar E_1t}\bra0\ket1+e^{-i\delta}e^{\frac i\hbar E_1t}e^{-\frac i\hbar E_0t}\bra1\ket0+3)$
> $=\frac14\hbar\omega_0(1+3)$
> $=\hbar\omega$

### 3.5.c. Other Operators

c.i. $\bra{\Psi,t}\hat x\ket{\Psi,t}$
> $\hat x=\sqrt{\hbar/2m\omega_0}(a+a^\dagger)$
> $\to\sqrt{\hbar/2m\omega_0}(\bra{\Psi,t}a\ket{\Psi,t}+\bra{\Psi,t}a^\dagger\ket{\Psi,t})$

One step at a time:
> $\bra{\Psi,t}a\ket{\Psi,t}$
> $\bra{\Psi,t}a(\frac1{\sqrt2}e^{-\frac i\hbar E_0t}\ket0+\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket1)$
> $\bra{\Psi,t}(\frac1{\sqrt2}e^{-\frac i\hbar E_0t}a\ket0+\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}a\ket1)$
> $(\frac1{\sqrt2}e^{-\frac i\hbar E_0t}\ket0+\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket1)^*(\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket0)$
> $(\frac1{\sqrt2}e^{\frac i\hbar E_0t}\bra0+\frac{e^{-i\delta}}{\sqrt2}e^{\frac i\hbar E_1t}\bra1)(\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket0)$
> $(\frac1{\sqrt2}e^{\frac i\hbar E_0t}\bra0)(\frac{e^{i\delta}}{\sqrt2}e^{-\frac i\hbar E_1t}\ket0)$
> $=\frac12e^{i((E_0-E_1)t/\hbar+\delta)}$
> $=\frac12e^{i(-\Delta E t/\hbar+\delta)}$
> $=\frac12e^{i(-\omega_0t+\delta)}$

Contrastly, $\bra{\Psi,t}a^\dagger\ket{\Psi,t}$:
> $=(\bra{\Psi,t}a\ket{\Psi,t})^*$
> $=\frac12e^{i(\omega_0t-\delta)}$

Add them up to get a really easy answer:
> $\braket x=\sqrt{\hbar/2m\omega_0}\cos(\omega_0t-\delta)$

c.ii. $\bra{\Psi,t}\hat p\ket{\Psi,t}$
> $\hat p=i\sqrt{m\hbar\omega_0/2}(-a+a^\dagger)$
> $=i\sqrt{m\hbar\omega_0/2}(-\bra{\Psi,t}a\ket{\Psi,t}+\bra{\Psi,t}a^\dagger\ket{\Psi,t})$
> $=i\sqrt{m\hbar\omega_0/2}(-\frac12e^{i(-\omega_0t+\delta)}+\frac12e^{i(\omega_0t-\delta)})$
> $=i\sqrt{m\hbar\omega_0/2}(i\sin(\omega_0t-\delta))$ 
> $=-\sqrt{m\hbar\omega_0/2}\sin(\omega_0t-\delta)$ 

### 3.5.x. Misc.

d. $\frac12\hbar\omega_0$ and $\frac32\hbar\omega_0$
> The different energy levels are obviously the eigenvalues of the Hamiltonian by definition (boomer theorem), so these are the values that will be collapsed to in the end.

e. $\frac32\hbar\omega_0\to\ket1$
> Without any explanation needed. It's literally the first energy level (not zero).

f. It depends on what energy is measured
> $\frac32\hbar\omega_0\to\frac1{\sqrt2}e^{-iE_1t/\hbar}\phi_1(x)$
> $\frac12\hbar\omega_0\to\frac1{\sqrt2}e^{-iE_0t/\hbar}\phi_0(x)$

g. $\braket{x}=\braket p=0$ because the particle collapses into either eigenstate which is fully symmetrical. The position and momentum operators shift the eigenstate up or down to dot product (to 1 instead of 0) with a now matching dual state. However the "matching" only happens when the wave-functions are in superposition. Otherwise the dot product have misaligned eigenstates and everything is just zero.

h. Just like how measuring different axis in the Stern-Gerlach experiment sets the originally measured basis into superposition, measuring the position puts the energy in superposition. The position operator also contains a creation operator, which could even raise the energy superposition of the particle past $\ket1$. So when you go to measure energy again, you could get a $\ket2$ state.

i. I learned about ladder operations and basis kets and why the Stern-Gerlach experiment on different axis works the way it does. Different measurements have eigenstates that hold other measurement eigenstates in superposition like we saw with the ladder operators. This kinda blew my mind. But it's obvious isn't it? I do wish I was able to derive those ladder things on my own though.