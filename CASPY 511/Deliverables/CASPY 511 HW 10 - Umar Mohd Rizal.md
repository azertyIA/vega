Given the Yukawa potential:
> $V(\vec r)=v_0\frac{e^{-br}}r$
> $k_0=\sqrt{2mE}/\hbar$
> $q=2k_0\sin\frac\theta2$

In the first Born approximation, we just take the FT of the potential to get things in terms of $q$
> $\iiint d^3r'e^{-i\vec q\cdot\vec r}\frac{e^{-br}}r$
> $=\iiint d^3r'e^{-i\vec q\cdot\vec r}\frac{e^{-br}}r$

> $\vec k_0=(k_0)(0,0,1)$
> $\vec k_f=(k_0)(\sin\theta\cos\phi,\sin\theta\sin\phi,\cos\theta)$
> $\vec q=\vec k_f-\vec k_0$
> $=(k_0)(\sin\theta\cos\phi,\sin\theta\sin\phi,\cos\theta-1)$
> $\vec r'=r'(\sin\theta''\cos\phi'',\sin\theta''\sin\phi'',\cos\theta'')$ (the angle between $\vec r'$ and $\vec q$)
> setting $\vec q\to\hat z$: $\vec q\cdot\vec r'=qr'\cos\theta''$

> $V(\vec q)=\iiint d^3r'e^{-i\vec q\cdot\vec r}\frac{e^{-br}}r$
> $=\int dr'r'^2v_0\frac{e^{-br'}}r'\int d\phi\int d\theta e^{-i\vec q\cdot\vec r}$
> $=\int dr'r'^2v_0\frac{e^{-br'}}r'\int d\phi\int d\theta e^{-iqr'\cos\theta}$
> $=\int dr'r'^2v_0\frac{e^{-br'}}r'\int d\phi\int -d(\cos\theta)/(\sin\theta) e^{-i\vec qr'\cos\theta}$ (u=cos theta), du = -sin theta dt
> $=2\pi\int dr'r'^2v_0\frac{e^{-br'}}r'\int d(\cos\theta) e^{-i\vec qr'}$
> $=2\pi\int dr'r'^2v_0\frac{e^{-br'}}r'(e^{-i\vec qr}+iq)e^{-i\vec qr'}$
