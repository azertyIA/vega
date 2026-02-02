The circuit symbol for an antenna is a dipole arrow. We don't care about the radiation near the antenna as the far away effects at an angle matters so much more, so the source basically becomes a point source.

One interesting idea is to put two of these dipoles orthogonal to each other, lying straight on the x and y axis. $\theta_A$ and $\theta_B$ help determine how the dipole is oriented on the xy plane. The dipole does not create waves that propagate in the direction that the dipole in oriented. Rather, the dipole contributes much more if the dipoles are orthogonal to where they should go. 

Imagine laying out a ruler. If the source is pretty far away the source then the trajectory looks like parallel waves. Putting antennas on each end of the ruler creates a difference between the antennas' phases. Which turns an approximately equal length to an issue, because the phases could definitely cancel out.
$$E_p=E_0+E_1:E_\theta|_{0,1}=jk\frac{Idl}{4\pi}(\frac{e^{-jkR}}R)\eta_0\sin\theta=E_mF(\theta,\phi)(\frac{e^{-jkR}}R)$$
$$\boxed{E_m=j\frac{Idl}{4\pi}\eta_0k:F(\theta,\phi)=\sin\theta}$$
$$E_p=E_mF(\theta,\phi)(\frac{e^{-jkR_0}}{R_0}+\frac{e^{-jkR_1}}{R_1})$$
$$=E_mF(\theta,\phi)(\frac{e^{-jkR_0}}{R_0}+\frac{e^{-jkR_1}e^{-j\xi}}{R_1}):(R_0-R_1)<<R_0$$

If we try to do find the angle between the antennas and the destination, it's not an easy plane. So, you have to parameterize the ground line with another set of theta and phi. 
$$\cos\alpha=\cos\theta\cos\theta'+\sin\theta\sin\theta'[\cos(\phi-\phi')]$$
In optimal conditions, the theta and phi of the ground ends up being a right angle (flat ground) and zero (aligned with the destination path). And the true change in distance can be found.
$$\cos\alpha=\cos\theta(0)+\sin\theta(1)[\cos(\phi-0)]=\sin\theta\cos\phi$$
$$\boxed{R_0-R_1\approx d\sin\theta\cos\phi}$$
And now you can arrive at your true electric wave sum:
$$E_p=E_mF(\theta,\phi)\frac{e^{-jkR_0}}{R_0}[1+e^{jkd\sin\theta\cos\phi}e^{j\xi}]$$$$=E_mF(\theta,\phi)\frac{e^{-jkR_0}}{R_0}[1+e^{j\Lambda}]:\Lambda=kd\sin\theta\cos\phi+\xi$$
$$=E_mF(\theta,\phi)\frac{e^{-jkR_0}}{R_0}e^{j\Lambda/2}(e^{-j\Lambda/2}+e^{j\Lambda/2})$$
$$=2E_mF(\theta,\phi)\frac{e^{-jkR_0+j\Lambda/2}}{R_0}\cos{\frac\Lambda2}$$
And the true magnitude of the sum.
$$|E_p|=\frac{2E_m}R|F(\theta,\phi)||\cos\frac\Lambda2|$$
The H-plane (horizontal plane) occurs when $\theta=\frac\pi2$. Truckers usually have two antennas that are some distance $d=\frac\lambda2$ apart with the controlled phase being $\xi=0$.
$$|E_p/E_{p.max}|=|\cos\frac12kd\cos\phi|=|\cos\frac\pi2\cos\phi|$$
This looks pretty bad, but we can just use the important points with obvious $\cos\phi$, and you'll get an egg figure eight. This is called the broad-side array. Because the rectangle faces the signal.

Another case is the BU Radio Station. which uses quarter wavelengths $d=\lambda/4$ with a delay of $\xi=-\pi/2$:
$$|E_p/E_{p.max}|=|\cos\frac12(kd\cos\phi+\xi)|=|\cos(\frac\pi4\cos\phi-\frac\pi4)|$$
This looks like a cardioid with maximum at $\phi=0,A=1$ and minimum $\phi=\pi,A=0$. This is called the end-fire pattern. So it aims in one direction.