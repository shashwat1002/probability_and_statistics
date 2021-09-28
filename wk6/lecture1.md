# Independent trials 

Probability of getting $k$ favorable results in $n$ independent trials: 

$$
{n \choose k} p^k (1-p)^{n-k}
$$

## Problem 

a coin for which P(HEADS) = p is tossed until two successive tails are obtained. Find the probability that the experiment ends in the nth trial 

Events: 

- $E_1$: first toss is H
- $E_2$: first two tosses are TH 
- $E_3$: first two tosses are TT

Note: these three form a partition on the whole space 

- $F_n$: experiment ends at nth trial 

Note: $n$ must be at least $2$

$$
P(F_2) = (1-p)^2
$$

for $n > 2$ 

So consider $P(F_n \mid E_1)$

Now, the thing is if H poses no restrictions on the next space, so any set of intervals can be said said to to be H followed by a smaller set of trials, so we get recursion.

with this we can say 

$P(F_n \mid E_1) = P(F_{n-1})$

consider $P(F_n \mid E_2)$

using similar arguments as above we can say 

$P(F_n \mid E_2) = P(F_{n-2})$

Now, consider $P(F_n \mid E_3) = 0$

because the game already ended at $n=2$ and we assumed $n>2$

By law of total probability, we have: 

for $n > 2$ 

\begin{equation}
    \begin{aligned}
        P(F_n) &= P(F_n \mid E_1)P(E_1) + P(F_n \mid E_2)P(E_2) + P(F_n \mid E_3)P(E_3) \\ 
        &= P(F_{n-1})P(E_1) + P(F_{n-2})P(E_2) \\ 
        & \text{recurrance relation }
    \end{aligned}
\end{equation}

# Properties of conditional probability 

for any event $A$, $B$, and $E$ we have the following: 

$$
0 \leq P(E \cap A) \leq 1
$$

$$
P(A \mid E) = 1 - P(A' \mid E)
$$


# Conditional events 

Two events $A$ and $B$ are conditionally independent given $E$ if 

$$
P(A \cap B \mid E) = P(A \mid E)P(B \mid E)
$$

# Random Variables 

## Example of random variable 

Let $X$ denote the outputs after we roll a die, then 

$X=3$ is an event 

and the probability of that event is referred to by 

$$
P(\{X=3\})
$$

means that after rolling a die, we obtain 3 as outputs

## Defining a random variable 

A random variable $X$ is a function from the sample space to the real numbers 

$X: S \rightarrow \mathbb{R}$

Note: 

- Random variables are not events 
- when a random variable is assigned a value, it becomes an event 


## Discrete Random Variable 

A Random Variable $X$ is discrete if the range in countable 

