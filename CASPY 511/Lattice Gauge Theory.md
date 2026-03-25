$$\hat H=\frac1{2m}(-i\hbar\nabla-qA(x))^2+q\Phi(x)$$
By default, trying to calculate the finite gradient computationally isn't gauge covariant (and kind of messed up) because after an arbitrary gauge transformation, the phases at different points could get misaligned and the physics is no longer preserved. As a result, we could try approximating the gauge covariant $(-i\hbar\nabla-qA)$ instead. 
$$\hat H=\frac1{2m}\hat D^2+q\Phi(x)$$
We could try factoring D.
$$D=-i\hbar\nabla-qA$$
$$=\lim_{a\to0}\frac1a[-i\hbar a\nabla-aqA]=\lim_{a\to0}\frac1a[(-i\hbar)(a\nabla)-(aqA)(1)]$$
$$=\lim_{a\to0}\frac1a[(-i\hbar)(a\nabla)+(-aqA)(1)+(-i\hbar)(1)+(-aqA)(a\nabla)-(-i\hbar)(1)-(-aqA)(a\nabla)]$$
$$=\lim_{a\to0}\frac1a[(-aqA-i\hbar)(1+a\nabla)-(-i\hbar)(1)-a^2(-qA)(\nabla)]$$
The $a^2$ term diminishes to zero much faster than anything else, and we'll derive in the x direction for now.
$$D_x\psi(x)=\lim_{a\to0}\frac1a[(-aqA-i\hbar)(1+a\partial_x)\psi-(-i\hbar)\psi]$$
$$=\lim_{a\to0}\frac{-i\hbar}a[(1-iaqA(x)/\hbar)(1+a\partial_x)\psi-\psi]$$
Because we are taking the limit to zero, we can collapse these first-order polynomials to exponential terms.
$$=\lim_{a\to0}\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}e^{a\partial_x}\psi-\psi]$$
$$=\lim_{a\to0}\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}\psi(x+a)-\psi(x)]$$
$$\approx\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}\psi(x+a)-\psi(x)]$$
We now have a new finite subtraction that could be gauge covariant. Let's see if it is. A typical gauge transformation transforms the following values as such.
$$\psi(x)\mapsto e^{iq\Lambda(x)/\hbar}\psi(x)$$
$$\psi(x+a)\mapsto e^{iq\Lambda(x+a)/\hbar}\psi(x+a)$$
$$A(x)\mapsto A(x)+\nabla\Lambda$$
Plugging in:
$$\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}\psi(x+a)-\psi(x)]$$
$$\mapsto\frac{-i\hbar}a[e^{-iaq(A(x)+\nabla\Lambda)/\hbar}e^{iq\Lambda(x+a)/\hbar}\psi(x+a)-e^{iq\Lambda(x)/\hbar}\psi(x)]$$
$$=\frac{-i\hbar}a[e^{-iaqA(x)/\hbar-iaq(\nabla\Lambda)/\hbar}e^{iq\Lambda(x+a)/\hbar}\psi(x+a)-e^{iq\Lambda(x)/\hbar}\psi(x)]$$
We now assume that $a\nabla\Lambda(x)\approx\Lambda(x+a)-\Lambda(x)$, or that $\Lambda$ is only linear.
$$\approx\frac{-i\hbar}a[e^{-iaqA(x)/\hbar-iq(\Lambda(x+a)-\Lambda(x))/\hbar}e^{iq\Lambda(x+a)/\hbar}\psi(x+a)-e^{iq\Lambda(x)/\hbar}\psi(x)]$$
$$=\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}e^{-iq(\Lambda(x+a)-\Lambda(x))/\hbar}e^{iq\Lambda(x+a)/\hbar}\psi(x+a)-e^{iq\Lambda(x)/\hbar}\psi(x)]$$
$$=\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}e^{iq\Lambda(x)/\hbar}\psi(x+a)-e^{iq\Lambda(x)/\hbar}\psi(x)]$$
$$=e^{iq\Lambda(x)/\hbar}(\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}\psi(x+a)-\psi(x)])=e^{iq\Lambda(x)/\hbar}D$$
This finite difference is gauge-covariant and the overall physics shouldn't change under any gauge transformation.
$$\boxed{D\psi(x)\approx\frac{-i\hbar}a[e^{-iaqA(x)/\hbar}\psi(x+a)-\psi(x)]=\frac{-i\hbar}a[T(x)\psi(x+a)-\psi(x)]}$$
But what about the other direction? It clearly needs to satisfy the same covariance under a gauge transformation:
$$\psi(x)\mapsto e^{iq\Lambda(x)/\hbar}\psi(x)$$
$$\psi(x-a)\mapsto e^{iq\Lambda(x-a)/\hbar}\psi(x-a)$$
$$A(x)\mapsto A(x)+\nabla\Lambda$$
Now let's guess some phase fixer for this:
$$\psi(x)-e^{F(x)}\psi(x-a)\mapsto e^{iq\Lambda(x)/\hbar}\psi(x)-e^{F(x)+iq\Lambda(x)/\hbar}\psi(x-a)$$
So let's just transform the left side and compare what is in the exponential:
$$\mapsto e^{iq\Lambda(x)/\hbar}\psi(x)-e^{F'(x)+iq\Lambda(x-a)/\hbar}\psi(x-a)$$
$$F'(x)+iq\Lambda(x-a)/\hbar=F(x)+iq\Lambda(x)/\hbar$$
In discrete space, we only have so many derivatives to encode the function properly. Thus, we should only do the derivative in one direction because we have previously approximated the derivative at $x$ to link $x+a$ and $x$. So we should use the derivative at $x-a$ to link $x$ and $x-a$.
$$=F(x)+iq\Lambda(x-a)/\hbar+iqa\nabla\Lambda(x-a)/\hbar$$
$$F'(x)=F(x)+iqa\nabla\Lambda(x-a)/\hbar$$
This phase definitely looks like the vector potential but around the $x-a$ link.
$$F'(x)=iqA'(x-a)/\hbar=iqA(x-a)/\hbar+iqa\nabla\Lambda(x-a)/\hbar$$
$$\boxed{D\psi(x)\approx\frac{-i\hbar}a[\psi(x)-e^{+iaqA(x-a)/\hbar}\psi(x-a)]=\frac{-i\hbar}a[\psi(x)-T^\dagger(x-a)\psi(x-a)]}$$
That's cool and all, but it's not squared yet... Let's first justify an anti-Hermitian, second-order friendly version of this (just by taking the average of both space directions):
$$D\psi(x)\approx\frac{-i\hbar}{2a}[T(x)\psi(x+a)-T^\dagger(x-a)\psi(x-a)]$$
$$=\frac{-i\hbar}{2a}[e^{-iaqA(x)/\hbar}\psi(x+a)-e^{+iaqA(x-a)/\hbar}\psi(x-a)]$$
$$e^{-iaqA(x)/\hbar}(D\psi)(x+a)=\frac {-i\hbar}{2a}e^{-iaqA(x)/\hbar}[e^{-iaqA(x+a)/\hbar}\psi(x+2a)-e^{+iaqA(x)/\hbar}\psi(x)]$$
$$=\frac {-i\hbar}{2a}[e^{-iaq(A(x)+A(x+a))/\hbar}\psi(x+2a)-\psi(x)]$$
$$e^{+iaqA(x-a)/\hbar}(D\psi)(x-a)=\frac{-i\hbar}{2a}e^{+iaqA(x-a)/\hbar}[e^{-iaqA(x-a)/\hbar}\psi(x)-e^{+iaqA(x-2a)/\hbar}\psi(x-2a)]$$
$$=\frac{-i\hbar}{2a}[\psi(x)-e^{+iaq(A(x-a)+A(x-2a))/\hbar}\psi(x-2a)]$$
$$\boxed{D^2\psi(x)=\frac {-\hbar^2}{4a^2}[e^{-iaq(A(x)+A(x+a))/\hbar}\psi(x+2a)+e^{+iaq(A(x-a)+A(x-2a))/\hbar}\psi(x-2a)-2\psi(x)]}$$
To check if this actually works, the offset A terms could very well be approximated to the first order using the displacement operator.
$$=\frac {-\hbar^2}{4a^2}[e^{-iaq(2A(x)+aA'(x))/\hbar}\psi(x+2a)+e^{+iaq(2A(x)-3aA'(x-a))/\hbar}\psi(x-2a)-2\psi(x)]$$
$$e^{ba(2A(x)+aA'(x))}\approx1+2baA(x)+ba^2A'(x)+2b^2a^2A^2(x)$$
$$e^{-ba(2A(x)-3aA'(x-a))}\approx1-2baA(x)+3ba^2A'(x)+2b^2a^2A^2(x-a)$$
$$\psi(x\pm2a)\approx\psi(x)\pm2a\partial_x\psi(x)+2a^2\partial_x^2\psi(x)$$
$$D^2\psi(x)=\frac{-\hbar^2}{4}[8bA(x)\partial_x\psi(x)+4\partial_x^2\psi(x)+4bA'(x)\psi(x)+4b^2A^2(x)]$$
$$=-\hbar^2\psi''+2iq\hbar A\psi'+iq\hbar A'\psi+q^2A^2$$
For computations sake, it wouldn't be bad to do this, but an extra halo to be allocated and fetched would pose much complexity to both initialization and the step routine. So, we can realize that the whole approximation wouldn't change very much if we put one of the $A'$ terms from the top to the bottom exponential as that would still result in $4$ total $A'$ terms.
$$e^{(2a)bA(x)}\approx1+2baA(x)+2b^2a^2A^2(x)$$
$$e^{-b(2a)(A(x-2a))}=e^{-ba(2A(x)-4aA'(x-a))}\approx1-2baA(x)+4ba^2A'(x)+2b^2a^2A^2(x-a)$$
And the whole Laplacian changes just a tiny bit.
$${D^2\psi(x)=\frac {-\hbar^2}{4a^2}[e^{-i(2a)qA(x)/\hbar}\psi(x+2a)+e^{+i(2a)qA(x-2a)/\hbar}\psi(x-2a)-2\psi(x)]}$$
But just enough for us to make one small substitution to simplify the entire equation: $a=2a$
$${=\frac {-\hbar^2}{a^2}[e^{-iaqA(x)/\hbar}\psi(x+a)+e^{+iaqA(x-a)/\hbar}\psi(x-a)-2\psi(x)]}$$
$$\boxed{D^2\psi(x)=-\frac {\hbar^2}{a^2}[T(x)\psi(x+a)+T^\dagger(x-a)\psi(x-a)-2\psi(x)]}$$
And the completed Hamiltonian step:
$$\boxed{H\psi(x)=-\frac {\hbar^2}{2m}[T(x)\psi(x+1)+T^\dagger(x-1)\psi(x-1)-2\psi(x)]+q\Phi(x)\psi(x)}$$
