The expected value is given by the "mean" answer given a probability distribution:
$$\mathbb E(X)=\Sigma xP_X(x)$$
$$ P_Y(y)=\Sigma_{g(x)=y} P_X(x)$$
### St Peterson's Game
Flip a coin and get tails until you get heads. For each tails, multiply your payout ($2) by 2. As a result, the expectation value actually blows up to infinity.
$$\mathbb E(X)=\Sigma (2^n)P_Y(2^n)=\Sigma1=\infty$$
$$\mathbb E(X)=\Sigma (2^n)P_Y(2^n)=\Sigma1=\infty$$
### Variance
Variance measures the expected value of the squared difference from the expected value. It tells you how much the distribution spreads over its domain.
$$Var[X]=\mathbb E[(x-\mathbb E[X])^2]=\Sigma(x-\mathbb E[X])^2P_X(x)$$
$$=\Sigma(x^2-2x\mathbb E[X]+\mathbb E[X]^2)P_X(x)$$
$$=\Sigma(x^2)P_X(x)-\Sigma2x\mathbb E[X]P_X(x)+\Sigma\mathbb E[X]^2P_X(x)$$
$$=E[X^2]-2\mathbb E[X](\Sigma xP_X(x))+\mathbb E[X]^2(\Sigma P_X(x))$$
$$=E[X^2]-2\mathbb E[X](\mathbb E[X])+\mathbb E[X]^2(1)$$
$$=E[X^2]-\mathbb E[X]^2$$

Some properties are as follows:
$$Var[aX+b]=a^2Var[X]$$
