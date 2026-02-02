## Foreshadowing

Start with the idea that you want to find some ordered approximation of a function if its parameter is perturbed. It would make sense to use a Taylor series:
$$f(t+\delta t)=\Sigma\frac{(\delta t)^n}{n!}\partial_t^nf(t)$$
$$=\Sigma\frac{(\delta t\partial_t)^n}{n!}f(t)$$
$$=\exp(\delta t\partial_t)f(t)$$
This weird looking exponential represents some evolution of the function over time. That's cool and all. So if we do end up finding some value that equals the time derivative of something, surely we can evolve in time.

## The Legendre Transformation

Generally, given a monotonic function of $y$, the Legendre Transformation returns the y-intercept of the linear approximation at a point in terms of the point's derivative.
$$f(x)\to f^*(\dot x)$$
$$f^*(\partial_xf)=x\partial_xf-f(x)$$
[[Lagrangian Mechanics]] blesses us with the following equations for the path of stationary action:
$$\partial_{\dot y}L=M,\partial_{y}L=\dot M$$
Trying to find the Legendre Transformation of the Lagrangian gets us this:
$$(L(y,\dot y))^*=L^*(y,\partial_{\dot y}L)=L^*(y,M)=\dot y(\partial_{\dot y}L)-L$$
$$\boxed{H(y,M)=\dot yM-L}$$
## Equations of Motion

We could also try finding the perturbation in this to find equations of motion:
$$\delta H(y,M)=\delta y\partial_yH+\delta M\partial_MH$$
$$=\delta(\dot yM-L)$$
$$=\delta(\dot yM)-\delta L$$
$$=\dot y\delta M+\delta\dot y M-\delta L(y,\dot y)$$
$$=\dot y\delta M+\delta \dot yM-\delta y\partial_yL-\delta{\dot y}\partial_{\dot y}L$$
$$=\dot y\delta M+\delta\dot y M-\delta y\dot M-\delta{\dot y}M$$
$$=\delta M\dot y-\delta y\dot M$$
$$\boxed{\partial_yH=-\dot M, \partial_MH=\dot y}$$
The equations of motion are quite symmetrical. Taking the derivative in one coordinate gets the time-derivative of the other.
## Free Particles

For a typical free particle, potential energy doesn't exist, but it's kinetic energy does:
$$L=K-U=mv^2/2-0$$
$$M=\partial_vL=mv$$
$$H=\dot xM-L=mv^2-mv^2/2=(mv)^2/2m=M^2/2m$$
Using the equation of motion:
$$\partial_x(M^2/2m)=0=\dot M$$
$$\partial_M(M^2/2m)=M/m=\dot x$$
Thus, $M$ is constant throughout time, and $x$ changes linearly over time.
## Harmonic Oscillator

Let's do a similar thing with a spring:
$$L=K-U=mv^2/2-kx^2/2,k>0$$
$$M=\partial_vL=mv$$
$$H=\dot xM-L=mv^2-mv^2/2+kx^2=M^2/2m+kx^2/2$$
Using the equation of motion:
$$\partial_x(M^2/2m+kx^2/2)=kx=-\dot M$$
$$\partial_M(M^2/2m+kx^2/2)=M/m=\dot x$$
$$\ddot x=\dot M/m=-kx/m$$
The trajectory follows the trajectory of $A\sin(\omega t)+B\cos(\omega t)$ where $\omega=\sqrt{k/m}$.

## Poisson Brackets

[[Poisson Brackets]] are a concept in linear algebra that encode the means of motion using differential equations.
$$\{A,B\}:=\partial_qA\partial_pB-\partial_pA\partial_qB$$
We can apply it to the Hamiltonian to get more symmetrical definitions for $\dot y$ and $\dot M$:
$$\dot M=0-\partial_yH$$
$$=(0)\partial_MH-(1)\partial_yH$$
$$\partial_t M=\partial_yM\partial_MH-\partial_MM\partial_yH=\{M,H\}$$
$$\dot y=\partial_MH$$
$$=(1)\partial_MH-(0)\partial_yH$$
$$\partial_t y=(\partial_yy)\partial_MH-(\partial_My)\partial_yH=\{y,H\}$$
In general, for an observable $f$, when the Hamiltonian is used in the Poisson Brackets:
$$\boxed{\partial_tf=\{f,H\}}$$
Alternatively putting two of the coordinates in the Poisson Brackets grants us unity:
$$\boxed{\{y,M\}=1}$$
