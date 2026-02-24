There's one fun law when it comes to conditional probability: 
$$P[A\cap B]=P[A|B]P[B]=P[B|A]P[A]$$
And with another fun law:
$$P[A]=P[\cup^i(A\cap B_i)]=\Sigma^i P[A\cap B_i]$$
Gets you the following rule that allows you to read probabilities of a single unknown event:
$$P[A]=P[B]\Sigma^i P[A| B_i]$$
### Variance and Expectation
The variance and expectation have linearity attached to them but otherwise, the probabilities you use would be conditional:
$$\mathbb E[x|B]=\Sigma xP_{X|B}(x)$$
$$Var[x|B]=\Sigma (x-\mathbb E[x|B])^2P_{X|B}(x)=\mathbb E[X^2|B]-\mathbb E[X|B]^2$$
