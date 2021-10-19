

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
\text{Var}(\alpha X) = \alpha^2 \text{Var}(X)
$$

Proof: 

$$
\begin{aligned}
    \text{Var}(\alpha X) &= E[\alpha ^2 X^2] - E[\alpha X]^2 \\
    & \text{ as expectation is linear, we have } \\
    &= \alpha ^2 E[X^2] + (\alpha E[X])^2 \\
    &= \alpha ^2 E[X^2] + \alpha ^2 E[X]^2 \\
    &= \alpha ^2 (E[X^2] + E[X] ^2) \\
    &= \alpha ^2 (\text{Var[X]})
\end{aligned}
$$

$$
Var(X+\alpha) = Var(X)
$$

Proof: 

$$
\begin{aligned}
    \text{Var}(X + \alpha) &= E[(X + \alpha)^2] - E[X+ \alpha]^2 \\
    &= E[X^2 + \alpha^2 + 2 \alpha X] - (E[X] + \alpha)^2 \\
    &= E[X^2] + \alpha ^2 + 2 \alpha E[X] - (E[X])^2 - \alpha ^2 - 2 \alpha E[X] \\
    &= E[X^2] - (E[X])^2 \\
    &= \text{Var}[X]
\end{aligned}
$$

Theorem: 

for the _independent variables_ $X_1, X_2 \dots X_n$ we have that 

$$
\text{Var}[X_1 + X_2 + \dots X_n] = \sum _{i=1} ^n \text{Var}[X_i]
$$

Proof: 

We'll prove this be induction 

Base case: $n=2$

we need to prove 

$$
\text{Var}[X_1 + X_2] = \text{Var}[X_1] + \text{Var}[X_2]
$$

LHS: 

$$
\begin{aligned}
    \text{Var}[X_1 + X_2] &= E[(X_1 + X_2)^2] - (E[X_1 + X_2])^2 \\
    &= E[X _1 ^2] + E{X _2 ^2} + 2E[X_1 X_2] - (E[X_1])^2 - (E[X_2])^2 - 2 E[X _1] E[X_2]
\end{aligned}
$$

We take a detour and consider $E[X_1 X_2]$

By definition of expectation we have 

$$
\begin{aligned}
    E[X_1 X_2] &= \sum _{\forall x_1}{\forall x_2} (x_1 x_2) P(X_1 = x_1 \cap X_2 = x_2) \\
    & \text{Since the variables are independent, we have } \\
    &= \sum _{\forall x_1}{\forall x_2} (x_1) P(X_1 = x_1) (x_2 )  P(X_2 = x_2) \\
    &= \sum _{\forall x_1} \Bigg( x_1 P(x_1) \Big(\sum _{\forall x_2} x_2 P(x_2) \Big) \Bigg) \\
    &= \sum _{\forall x_1} \Bigg( x_1 P(x_1) E[X_2] \Bigg) \\
    &= E[X_1]E[X_2]
\end{aligned}
$$

We substitute this to where we left the proof 

$$
\begin{aligned}
    \text{Var}[X_1 + X_2] &= E[X _1 ^2] + E{X _2 ^2} + 2E[X_1 X_2] - (E[X_1])^2 - (E[X_2])^2 - 2 E[X _1] E[X_2] \\
    &= E[X _1 ^2] + E{X _2 ^2} + 2E[X_1] E[X_2] - (E[X_1])^2 - (E[X_2])^2 - 2 E[X _1] E[X_2] \\
    &= E[X _1 ^2] - (E[X_1])^2 + E[X _2 ^2] - (E[X_2 ^2]) \\
    &= \text{Var}[X_1] + \text{Var}[X_1]
\end{aligned}
$$

Base case proved.

Induction hypothesis: 

For an arbitrary $k > 2$

$$
\text{Var} [\sum _{i=2} ^k X_i] = \sum _{i=2} ^k \text{Var}[X_i]
$$

Such that all $X_1, X_2 \dots X_k$ are all independent events. 

We need to prove that $\text{Var}[\sum _{i=1} ^{k+1} X_i] = \sum _{i=1} ^{k+1} \text{Var}[X_i]$

given that $X_1 \dots X_{k+1}$ are independent random variables, therefore we can say that $X_1 + \dots + X_k, X_{k+1}$ are also independent and thus, we have: 

$$
\begin{aligned}
    \text{Var}[\sum _{i=1} ^{k+1} X_i] &= \text{Var}[\sum _{i=1} ^k X_i + X_{k+1}] \\
    & \text{ and by base case, we have } \\
    &= \text{Var}[\sum _{i=1} ^k X_i] + \text{Var}[X_{k+1}] \\
    & \text{ using the induction hypothesis, we get } \\
    &= \sum _{i=1} ^k \text{Var}[X_i] + X_{k+1} \\
    &= \sum _{i=1} ^{k+1} \text{Var}[X_i]
\end{aligned}
$$

Hence proved 



# Higher order moments and moment generating function 

Defined as 

$$
M_X(t) = E[e^{tX}] = \sum _x e^{tx} p_X(x)
$$

Lemma: 

- $M_X(0) = 1$
- $E[X] = M'_X(0)$ where $'$ means derivative w.r.t $t$