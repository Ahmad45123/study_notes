# Total Probability Rule
It allows one to express the probability of any event in terms of conditional probabilities.

$$ P(E) = P(F).P(E | F) + P(F^\prime).P(E | F^\prime) $$
such that

$$ F \cup  F^\prime = S \ \& \  F \cap F^\prime = \phi $$

And generally, suppose S is represented as a set of $n$ disjoint events $F_k$: 

$$ P(E) = \sum_{k=1}^n P(F_k) . P(E | F_k)$$

# Bayes' Theorm

- $A$ is event of sample space $S$.
- Let $B_i$ be $n$ events such that: 
  - One of them must occur
  - $B_i$ and $B_j$ cannot occur together.
  - $S$ is the union of all $B$s.

$$ P(B_n | A) = \frac{P(B_n) . P(A | B_n)}{\sum_{i=1}^n P(B_i) . P(A | B_i)} $$

# Examples
- The probability of a system to function when there's $n$ components connected in parallel and the probability of failure is $p_k$: $\bold{1 - \prod_{k=1}^n p_k}$
- When a system functions if atleast k-out-of n components work, the probability is: $\sum_{j=k}^n P(E_j)$ where $P(E_j)$ is the probability that exactly $j$ components function. $P(E_j) = nCj . (1-p)^j . p^{n-j}$