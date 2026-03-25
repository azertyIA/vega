#PY511
It all starts with the Stern-Gerlach Experiment. Cuz why wouldn't it?

When shooting a beam of silver atoms through a magnetic field setup, you get two beams rather than a shmear. 

Then there's the Double Slit Experiment. Putting electrons through a diffraction pattern makes it result in a pattern of interference.

Heisenberg didn't like the spectral lines. Why were there doublets? Triplets? Why did hydrogen only have four spectral lines?

Starting with a quantum particle, there were only two "fake" properties: color (**Y**ellow or **G**reen) and shape (Ball-0, and Rod-1).

So obviously there are four possibilities given 2x2 options. You could send in the particles through a separator (don't worry about the details) of color and shape, separately.

This is different from measurement. Just because.

One would expect if you just put particles straight in the sort would be split 50-50 in general. If you put the same sorter in series, you would get a very predictable result. (Putting a color sorter in front of the green output will be fully green).

Putting two different ones in series would result in another 50-50 if the two properties are uncorrelated. 

Most interestingly, if you sandwich a sorter with two different sorters, the state resets?
> IN -> Color -> Shape -> Color -> 50/50

But WHY? Has math failed us?

This is a very rough analogue of real life, except instead of two of these properties is just axis of "quantum spin."
> IN -> SGz -> SGx -> SGz -> 2 Beams

## Waves

Photons, electrons and most elementary particles are best described as waves of probability. (Or excitation) Determinism rarely exists.

The probability distribution of a Higgs Boson, for example, looks like a fuzzy ball. But we only see tracks and rays. The boson has a mass of 125.1 $GeV/c^2$

Carl Anderson captured the positron by literally putting a piece of lead in a magnetic field to slow such a projectile. We only see tracks, but we can still do so much with such a thing.

## 

## Mach-Zehnder Interferometer

Two beam splitters and two mirrors, opposite to each other in a diamond shape. Shoot some light and see what you get when it gets to the second beam splitter. Black box the contraption and know that input is 1 and 0, and the resulting amplitudes will be $\alpha$ and $\beta$. Naturally just group them.

Group them into vectors, so a 2x2 matrix will be needed to transform one into the other:
> $\begin{bmatrix}? & ? \\ ? & ?\end{bmatrix}\begin{bmatrix}\alpha \\ \beta\end{bmatrix}=\begin{bmatrix}\alpha' \\ \beta'\end{bmatrix}$

The beam splitter by itself has Reflectivity and Transmissivity or *Fresnel coefficients*, set by certain physical properties. Dielectric thin films on multiple layers provide enormous flexibility.

The mirrors are just some identity matrix times a coefficient.

Putting it all together:
> $B_2\cdot M\cdot B_1\cdot\begin{bmatrix}\alpha \\ \beta\end{bmatrix}=\begin{bmatrix}\alpha' \\ \beta'\end{bmatrix}$

One set of physical properties will result in a specific defined answer.

You could put a blocker in there to "kill" the beam which would just be a pretty simple matrix:
$K=\begin{pmatrix}1 & 0 \\ 0 & 0\end{pmatrix}$

However, now you get that a quarter of the photons end up at each detector, as half the photons are lost.

### BOMB

Each bomb has a fuse with a dye that absorbs a photon, and explodes the bob. Half the bombs have defective fuses in which the due was omitted, so the bomb won't go off. Can you identify at least one working bomb without blowing it up?

