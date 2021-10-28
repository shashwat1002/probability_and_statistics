# Definition of Cumulative Distribution Function 

## Definition 

The _cumulative distribution function (CDF)_ of a random variable $X$ is defined as 

$$
F_X(x) = P(X \leq x) \forall x \in \mathbb{R}
$$

- The subscript $X$ indicates that this is the CDF of the random variable $X$ 

- the CDF is defined for all $x \in \mathbb{R}$

Example of CDF 





## Remarks on CDF 

- Let $X$ be a discrete Random Variable with range $R_X = \{x_1, x_2, \dots \}$

- Here we assume $x_1 < x_2 < \dots$ 

- CDF _stays flat_ in $X_k$ and $x_{k+1}$

A result 

For all $a \leq b$ we have 

$$
P(a < X \leq b) = F_X(b) - F_X(a)
$$


Note: can't get point wise probability for continuos variables 


Uniformity of continuos variable implies that 

$$
P(X \in [x_1, x_2]) \propto (x_2 - x_1) \text{where } a\leq x_1 \leq x_2 \leq b
$$

# Continuos Random Variable 

A Random variable $X$ with CDF $F_x(x)$ is said to be continuos if $F_X(x)$ is a continuos function for all $x \in \mathbb{R}$


# Probability Denisty functions 

- The probability density functions (PDF) would be defined as probability per unit length 

- Consider a continuos random variable $X$ and define $f_X(x)$ as follows: 

$$
f_X(x) = \lim _{\Delta \to 0^+} \frac{P(x < X < x+ \Delta)}{\Delta}
$$

- Here $f_X(x)$ gives the probability density at point $x$


