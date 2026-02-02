Independence also has just one rule, which makes many calculations easy (flipping coins):
$$P[A\cap B]=P[A]P[B]$$
But this can be decomposed into two different checks by dividing by the probability of either:
$$P[A|B]=P[A]$$
$$P[B|A]=P[B]$$
In other words there is no correlation between two different events. This is different between two mutually exclusive events which is where there is no intersection between two events (like partitions, which are also not independent). 

It's also important to note that $P[A]$ and $P[B]$ is influenced by the entire sample space and is often difficult to obtain. To throw in a third, you cannot use transitive property. To find independence more than two events, you can encode the problem by using:
$$P[A\cap B\cap C]=P[A]P[B]P[C]$$
But you also need to check the independence between each pair as well (*pairwise independence*). If you have pairwise independence, then you need to use more than one event to get a better guess of the other.