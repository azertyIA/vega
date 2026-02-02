Apparently quantum stuff is actually random but statistics is just more about attributing understanding to uncertainty. Given two different paths of wireless signal paths, you're gonna get two different phases. This results in an oscillating resulting diffraction pattern, that changes very fast.

### Probability
If an event always occurs then its probability is 1. If the event never occurs, then its probability is 0. This is a naive approach. Other approaches feature sample spaces and equal probabilities to partition out a result.

The modern axioms are probabilities are:
1. A sample space are all possible outcomes. $P[\Omega]=1$
2. An event is a subset of the sample space. 
3. Negative probability does not exist. $P[A]\geq0$

Our computers back then sucked pretty badly. Some modern applications are LLMs (but that's just linear algebra), recommendation systems and biomedical dataset parsing.

Given two overlapping events in sample space, the **union** ($\cup$) shows what's in either and the intersection shows what's in both. The complement describes what is not in either. De Morgan's Rules demonstrates that the complement of the operation is found by flipping the operations. 

In the example of three coins (heads or tails three times), there are eight possible universes and the probability of one specific event is thusly $1/8=0.125$. For instance, the probability you get three heads is $0.125$. Exactly two heads is $0.375$ because of the three outcomes for just one tails. At least two heads is the addition of the two previous cases: $0.500$.
$$\boxed{P[A\cap B]=P[A]+P[B]-P[A\cup B]}$$