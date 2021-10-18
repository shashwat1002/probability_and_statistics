

## Expectations of Poisson

\begin{equation}
    P_X(k) = 
    \begin{cases}
        \frac{e^{-\lambda } \lambda^k}{k!} & k \in R_X \\ 
        0 & \text{ otherwise }
    \end{cases}
\end{equation}


Show that the expectation $E[X] = \lambda$

Proof: 

TODO 



## Expectation of Binomial Distribution

We need to show that $E[X] = np$ 

Given that 

\begin{equation}
    P_X(k) = 
    \begin{cases}
        {n \choose k} p^k (1-p)^{n-k} & \forall k=0, 1, \dots, n \\
        0 & \text{otherwise}
    \end{cases}
\end{equation}

Proof: 

$$
\begin{aligned}
    E[X] &= \sum_{x=0} ^n x {n \choose x} p^x q^{n-x} \\
    &= \sum _{x=0} ^n x \cdot \frac{n!}{(n-x)!x!} p^x q^{n-x} \\
    &= 0 + \sum _{x=1} ^n x \cdot \frac{n!}{(n-x)!x!} p^x q^{n-x} \\
    &= 0 + \sum _{x=1} ^n \cdot \frac{n \cdot (n-1)!}{((n-1) - (x-1))! (x-1)!} p \cdot p^{x-1} q^{(n-1)-(x-1)} \\
    & \text{Let} x-1 = r \\
    &= np \sum_{r=0} ^{n-1} {(n-1) \choose r} p^r q^{n-1-r} \\
    &= np (p+q)^{n-1} \\
    &= np
\end{aligned}
$$





# Variance 

## Motivation of Variance 

- expectation is also called mean of a random variable. 'tis not a very good measure of how $X$ is distributed

To show you an issue with expectation: 

- You get 1000
- A fair coin is tossed, you get 2k for heads
- A number is chosen from 1 to 1k and if oyu guess it you get a million 


all have the same expectation: 1000

Let $\mu = E[x]$. The variance $Var(X)$ of $X$ is defined by 

$$
Var(X) = E((X-\mu)^2) = \sum _x (x-\mu)^2 f_X(x)
$$

Theorem: 

If $X$ is a discrete random variable with mean $\mu$ then 

$$
\text{Var}(X) = E[x^2] - \mu ^2
$$


(proof by linearity is ez)

Theorem: 

$$
\text{Var}(\alpha X) = \alpha^2 \text{Vanr}(X)
$$

$$
Var(X+\alpha) - Var(X)
$$

# Higher order moments and moment generating function 

Defined as 

$$
M_X(t) = E[e^{tX}] = \sum _x e^{tx} p_X(x)
$$

Lemma: 

- $M_X(0) = 1$
- $E[X] = M'_X(0)$ where $'$ means derivative w.r.t $t$