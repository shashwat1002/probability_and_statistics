# Random Variables (continued)

## Types 

- Discrete 
- Continuos 
- mixed (will be defined later)

# Probability Mass function 

## Definition 

Let $X$ be a random variable with range $R_X = \{x_1, x_2, \dots \}$ which is either finite or countable finite. Then the function we define as: 

$$
P_X(x_k) = P(X=x_k), \forall k=1, 2 \dots 
$$

is called the probability mass function 

for discrete variables it is also called the probability distribution 


## Properties of PMF 

1. $0 \leq P_X(x) \leq 1\ \forall \ x$ 
2. $\Sum_{x \in R_x} P_X(x) = 1$ (note: the entire sample space is covered because random variables are defined a a function $S \rightarrow \mathbb{r}$ and that by the definition of a function implies that the entirety of $S$ must be covered (the domain))
3. 

# Independent random variables 

We Consider two random variables _independent_ if 

$$
P(X = x, Y = y) = P(X=x)P(Y=y), \ \forall x, y
$$

# Expectation 

## Definition 

expected value of random variable is 

$$
\sum_{x \in R_X} P_X(x) \cdot x
$$

## Expectation is linear 

$$
E[aX + b] = aE[X] + b
$$

because expectation of a constant is the constant itself 




