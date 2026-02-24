Let's go back to Faraday's Law. Most of power electronics is inductors, so Faraday's Law is super essential. 
### General Lab Safety
Make sure to wear the right boots. Make sure to use the right power-rated resistors or else there will be fires. 
> A lot of the stuff comes straight from Australia. So apparently it was a fun learning experience to repair the thing.
### Semi-Empirical Faraday's Law
The earliest iterations of Faraday's Law came from multiple experiments of Faraday himself. 
$$\nabla\times\vec E=-\partial_tB$$
$$\iint d\vec s\cdot(\nabla\times\vec E)=\oint d\vec l\cdot\vec E=-\partial_t\Phi_B=-\partial_t\iint d\vec s\cdot\vec B$$

What is an electric circuit? A circuit comes with analysis (I-V characteristics) and execution as hardware. To tackle analysis we need models because models turn phenomena into equations. For instance we assume that resistors are pure resistors. And then you actually build the circuits as hardware.
### Don't Trust Diagnostic Instruments
There are a few probes, but there is a general rule of thumb. **Diagnostic instruments are not supposed to skew the data.** 

Kirchhoff's Voltage Law deals with **conservation of energy**, but the Kirchhoff's Current Law deals with **conservation of charge**, with the *mechanism that charge cannot be accumulated in one place*. 

### Lenz's Law
Let's say we have four nodes separated by two resistors in a ring. There was no voltage drop between two nodes anywhere without the magnetic field. However, when there was a magnetic field, there was a current running through the things. Faraday's law definitely obeys the conservation of energy.
$$\nabla\times\vec E=-\partial_tB$$
$$\iint d\vec s\cdot(\nabla\times\vec E)=\oint d\vec l\cdot\vec E=-\partial_t\Phi_B=-\partial_t\iint d\vec s\cdot\vec B$$
This process is given by Stokes' Theorem. The units of the electric field integrated across a distance is voltage. So, a changing magnetic flux leads to an induced voltage. Magnetic fields separate charges in a moving conductive rod. Charge separation leads to electric fields that want to "oppose" the magnetic fields around it.