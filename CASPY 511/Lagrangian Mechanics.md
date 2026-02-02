## Action

Lagrangian mechanics has much to do with the trajectories or paths a particle can take. To unlock this theory of mechanics from Newtonian mechanics, note that force is a consequence of potential.
$$\nabla U=-m\ddot y$$
In a simple case for the optimal true trajectory, let's perturb the path across time except for the endpoints: 
$$\nabla U\delta y=-m\ddot y\delta y$$
$$\delta U=-m(\ddot y\delta y+\dot y\delta\dot y-\dot y\delta\dot y)$$
$$\delta U=-m(\partial_t(\dot y\delta y)-\dot y\delta\dot y)$$
$$\int dt\delta U=-m\int dt\partial_t(\dot y\delta y)+m\int dt\dot y\delta\dot y$$
$$\int dt\delta U=-m\dot y\delta y|_{t_0}^{t_1}+m\int dt\dot y\delta\dot y$$
The first term on the right-hand side evaluates to zero because the perturbation is zero at the endpoints or at the time start and the time end:
$$\int dt\delta U=m\int dt\dot y\delta\dot y$$
$$\int dt\delta U=\frac m2\int dt(\delta\dot y\dot y+\dot y\delta\dot y)$$
$$\int dt\delta U=\frac m2\int dt\delta(\dot y^2)$$
$$0=\int dt(-\delta U)+\delta(\frac m2\dot y^2)$$
$$0=\delta\int dt(K-U)$$
We call the integrand the Lagrangian $L(t,y,\dot y)$ and the result of the integral the action $S$. Thus, the correct path, according to Newtonian mechanics, is a path of stationary action:
$$\boxed{0=\delta\int dt(K-U)=\delta\int dtL(y,\dot y)=\delta S}$$
## Euler-Lagrange Equation

Assume that the path of least action $y$ is perturbed with $\epsilon\eta(t)$:
$$y'=y+\delta y=y+\epsilon\eta$$
We can start by using the partial derivative linear approximations:
$$L(y+\delta y,\dot y)=(1+(\delta y)\partial_y)L(y,\dot y)$$
$$L(y,\dot y+\delta \dot y)=(1+(\delta\dot y)\partial_{\dot y})L(y,\dot y)$$
So we can crack the resulting Lagrangian:
$$L(y',\dot y')=L(y+\delta y,\dot y+\delta\dot y)$$
$$=(1+(\delta y)\partial_y)L(y,\dot y+\delta\dot y)$$
$$=(1+(\partial_t\delta y)\partial_{\dot y})(1+(\delta y)\partial_y)L(y,\dot y)$$
$$=(1+\epsilon(\partial_t\eta)\partial_{\dot y})(1+\epsilon\eta\partial_y)L(y,\dot y)$$
$$=((1+\epsilon\eta\partial_y)+\epsilon(\partial_t\eta)(\partial_{\dot y}+\epsilon\eta\partial_{\dot y}\partial_y))L(y,\dot y)$$
$$=(1+\epsilon\eta\partial_y+\epsilon(\partial_t\eta)\partial_{\dot y}+O(\epsilon^2))L(y,\dot y)$$
$$=(1+\epsilon\eta\partial_y+\epsilon(\partial_t\eta)\partial_{\dot y}))L(y,\dot y)$$
The difference in action is thusly:
$$S'-S=\int dt(L(t,y',\dot y')-L(y,\dot y))$$
$$=\int dt(\epsilon\eta\partial_y+\epsilon(\partial_t\eta)\partial_{\dot y})L(y,\dot y)$$
$$=\epsilon\int dt(\eta\partial_y+(\partial_t\eta)\partial_{\dot y})L(y,\dot y)$$
But because $y$ in this case represents the least action, the derivative here ($\Delta S/\epsilon$) should be approximately zero to represent the minimum. So we already know the result of this integral:
$$\delta S=0=\int dt(\eta\partial_y+(\partial_t\eta)\partial_{\dot y})L(y,\dot y)$$
$$=\int dt(\eta\partial_yL+(\partial_t\eta)\partial_{\dot y}L)$$
$$=\int dt(\eta\partial_yL+(\partial_t\eta)\partial_{\dot y}L)$$
$$=\int dt(\eta\partial_yL+(\partial_t\eta)\partial_{\dot y}L+\eta\partial_t\partial_{\dot y}L-\eta\partial_t\partial_{\dot y}L)$$
$$=\int dt(\eta\partial_yL+\partial_t(\eta\partial_{\dot y}L)-\eta\partial_t\partial_{\dot y}L)$$
$$=\eta\partial_{\dot y}L|^{t_1}_{t_0}+\int dt(\eta\partial_yL-\eta\partial_t\partial_{\dot y}L)$$
But the change in path overall shouldn't deviate from the original path if they have the same endpoints, so the non-integral term is just 0.
$$0=\int dt(\eta\partial_yL-\eta\partial_t\partial_{\dot y}L)$$
$$=\int dt\eta(\partial_yL-\partial_t\partial_{\dot y}L)$$
After factoring out the time-dependent term, we find that the bracketed term must be 0 in order for all functions of $\eta$ to integrate to zero. And a new equation of motion is born anew, where $M$ is defined as the canonical momentum:
$$0=\partial_yL-\partial_t\partial_{\dot y}L$$
$$\boxed{\partial_{\dot y}L=M,\partial_yL=\dot M}$$
## Free Particles

For a typical free particle, potential energy doesn't exist, but it's kinetic energy does:
$$L=K-U=mv^2/2-0$$
$$M=\partial_vL=mv$$
Using the equation of motion:
$$\partial_x(mv^2/2)=\partial_t(mv)$$
$$0=\partial_tv$$
Thus, $v$ is constant throughout space.

## Harmonic Oscillator

Let's do a similar thing with a spring:
$$L=K-U=mv^2/2-kx^2/2,k>0$$
$$M=\partial_vL=mv$$
Using the equation of motion:
$$\partial_x(mv^2/2-kx^2/2)=\partial_t(mv)$$
$$-(k/m)x=\partial_t^2x$$
$$0=(\partial_t^2+k/m)x$$
The trajectory follows the trajectory of $A\sin(\omega t)+B\cos(\omega t)$ where $\omega=\sqrt{k/m}$.