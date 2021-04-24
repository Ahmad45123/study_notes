# Mutually Eclusive Events
Two events are called mutually exclusive if 

$$E \cap F = \emptyset$$

- Drawing a club and then a heart are **mutually exclusive**.
- Drawing a club and drawing a king are **NOT** mutually exclusive.

# Probability
$$  P(E) = \frac{N(E)}{N(S)} $$

> If all the outcomes of events are NOT equally likely to occur, we use the so-called Empirical or Subjective probabilities.

## Addition Rule
$$ P(E \cup F) = P(E) + P(F) - P(E \cap F)$$

### How about 3 events ?
We must add the part that was removed twice.

$$ P(E \cup F \cup G) = P(E) + P(F) + P(G) \\ - P(E \cap F) - P(E \cap G) - P(G \cap F) \\ + P(E \cap F \cap G)$$

## Complementary Event

$$ E^\prime = S \setminus E$$
The "$\bold{\setminus}$" denotes set difference.

> It's clear that $E$ and $E^\prime$ are mutually exclusive.

$$ P(E^\prime) + P(E) = 1$$

## De Morgan Laws
$$ (E \cup F)^\prime = E^\prime \cap F^\prime $$

$$ (E \cap F)^\prime = E^\prime \cup F^\prime $$

## Joint Probability
$$ P(A\ and\ B) = P(A \cdot B) = P(A \cap B) $$

Events are ***independent*** if the occurance of one event doesn't affect the occurence of another.

$$ P(A\ and\ B) = P(A) \cdot P(B)$$

> Events are **mutually exclusive** when the occurrence of any one event implies that none of the others can occur at the same time: i.e., $P(A\ and\ B) = 0$.

## Conditional Probability

