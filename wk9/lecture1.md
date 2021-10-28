
# Higher order moments 

## Define the nth moment 

The nth moment about the mean or the nth central moment of a real values random variable $X$ is: 

$$
\mu _n = E[(X - E[X]) ^n]
$$

Where $E$ is the expectation operator 

The $\mu _0$ is just $1$

The first central moment $\mu_1$ is expectaion 

and $\mu_2$ is just variance 


# Moment Generating Function 

The moment generating function $M_X(t)$ is: 

$$
M_X(t) = E[e^{tX}] = \sum _x e^{tx} P_X(x)
$$

Lemma: 

- $M_X(0) = 1$
- $E[X] = M'_X(0)$ where $`$ is the derivative

## Moment generating function for the Binomial Distribution 

$$
\begin{aligned}
    M_X(t) &= \sum _{x=0} ^n {n \choose x} p^x (1-p) ^{n-x} e^{tx} \\
\end{aligned}
$$



## Variance using Moment Generating Function 

$$
\text{Var}(X) = M'' _X(0) - (M' _X (0))^2
$$


$$
\begin{aligned}
    \text{Var}(X) = E[(X - E[X])^2]
\end{aligned}
$$

$$
\begin{aligned}
    &M_X(t) = \sum _x e^{tx} p_X(x) \\
    & \implies M' _X(t) x \sum_x e^{tx} p_X(x) \\
    & \implies M'' _X (t) = x^2 \sum _x e^{tx} P_X (x) 
\end{aligned}
$$

and now we get 

