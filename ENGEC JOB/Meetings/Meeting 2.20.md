There are three aspects for cybersecurity: confidentiality, integrity, and authenticity. There are usually three parties involved. Alice encrypts their data, and try to exchange keys while the adversary, Eve, attempts to hijack the other parties.

Zero Knowledge Proofs help with the integrity aspect of cybersecurity. The prover proves that a certain claim is true without revealing any additional information about the claim. The verifier can be convinced that the prover has a good 3-coloring solution if the prover just shows two colors without revealing something else, repeatedly.

In a ZKP system, a program is compiled to an arithmetic circuit. The prover makes some polynomials and is verified later on. Because its being communicated, the proof better be small. 

For example we can hash the vector elements with each other a ton to make a hashed version of the vector, which is sent to the verifier. The verifier asks for something and the prover sends the surrounding minimum data needed to achieve the same hash.

The prover needs four gadgets:
1. zero test: prove that the function is identically 0 on all elements.
	1. $q(x)\to f(x)/Z_\Omega(x)$
	2. ask for q(r) not on Z
	3. send f(r), q(r) and proofs
2. product check: prove that the product of the function on all inputs is 1.
	1. generate $\hat t$ such that $t(1)$=$f(1)$ and $t(\omega^k)=\Pi f(\omega^i)$ 
	2. send $f(r)$, $q(r)$ and proofs
3. permutation test: proves that two function are permutations of each other.
	1. P: $\hat f=\Pi(x-f(a))$ and $\hat g=\Pi(x-g(a))$
	2. product check on f/g
4. prescribed permutation: proves that f and g follow a specific permutation.
	1. prove that $f=g(W(y))$
	2. P: $\hat f=\Pi(x-f(a))$ and $\hat g=\Pi(x-g(a))$
A vanishing polynomial looks like $Z_\Omega(x)=\omega^x-1$ where roots of unity are used.

So now let's make a proof for a real program. Let's say that there are two p values and one v value and generate a transcript with some stuff. Then interpolate a degree (table - 1) polynomial by encoding all the inputs (in the negative direction) and gates (spaced by three in the positive direction). 

The prover just needs to generate the transcript polynomial and hash it to the verifier. 
1. T encodes the correct inputs
	1. make a polynomial for the inputs $R(x)$ 
	2. do a zero test on $T(x)-R(x)$ for all inputs
2. Every gate is evaluated properly
	1. S(output gate)=1/0 if addition/multiplication
	2. Prove that $S(y)[T(y)+T(\omega y)]+[1-S(y)]T(y)T(\omega y)+...$
3. Wiring is implemented correctly
	1. permute the shits
4. And the output is expected