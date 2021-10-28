---
header-includes:
    - \usepackage{esdiff}
---


The function is non decreasing 

# Probability Density Function 

Probability per unit (length on the graph)

$$
\text{PDF} = \diff{\text{CDF}}{x}
$$

Note that we don't need CDF to be differenciable at all points because we can always defined PDF piecewise 

thus consider a continuos random variable $X$ and we define $f_X(x)$ as follows 

$$
f_X(x) = \lim _{\Delta \to 0^+} \frac{P(x < X \leq x + \Delta)}{\Delta}
$$


## Properties of PDF 

since PDF is the derivative of CDF, we have: 


$$
F_x(x) = \int _{\infty} ^\infty f_X(u) du
$$

where $F_X(x)$ is the CDF 

which means that 

$$
P(a < X \leq b) = F_X(b) - F_X(a) = \int _a ^b f_X(u) du
$$



- $f_X(x) \geq 0 \ \forall x \in \mathbb{R}$ because it a derivative of a non decreasing function 

- $\int _{-\infty} ^\infty f_X(u) du = 1$ 

- $P(a < X \leq b) = F_X(b) - F_X(a) = \int _a ^b f_X(u) du$

- More generally, for a set $A$, $P(x \in A) = \int _A f_X(u) du$


## Range, Expectation, and Variance of a Continuos Random Variable 


### Definition: Range 

The range of a random variable $X$ is the set of possible values of the random variable. If $X$ is a continuos random varible

$$
R_x = \{x | f_X(c) > 0 \}
$$

where $f_X(x)$ is the PDF 

### Definition: Expected Value of a Continuos R.V. 

Since in the discrete case we were doing a summation of x times f(x), here that'll change to an integration 

$$
E[X] = \int _{\infty} ^\infty x f_X(x) dx
$$

#### Example of this 

Let $X \sim \text{Uniform} (a, b)$ Find $E[X]$ 

We know that 

$$
f_X(x) = 
\begin{cases}
    \frac{1}{b-a} & a < x < b \\
    0 & \text{otherwise}
\end{cases}
$$

and thus 

$$
\begin{aligned}
    E[X] &= \int _{-\infty} ^\infty x f_X(x) \\
    &= \int _b ^a x \cdot \frac{1}{b-a} \\
    &= \frac{b^2 - a^2}{2(b-a)} \\
    &= \frac{b+a}{2}
\end{aligned}
$$

### Expected value of a function of a continuos random variable 

$$
E [ g(X)] = \int _{- \infty} ^ \infty g(x) f_X(x) dx
$$

Note that the linearity holds as well 

- $E[aX + b] = aE[X] + b \ \forall a, b \in \mathbb{R}$

- $E[X_1 + X_2 + \dots + X_n] = E[X_1] + E[X_2] + \dots + E[X-n]$


#### Example 

Let the PDF of a continuos RV be given by 

$$
f_X(x) = 
\begin{cases}
    x + \frac{1}{2} & 0 \leq x \leq 1 \\
    0 & \text{otherwise }
\end{cases}
$$

We need to find $E[X^n]$

$$
E[X^n] = \int _{-\infty} ^\infty x^n f(x) dx = \int _0 ^1 x^n \Big(x + \frac{1}{2} \Big)
$$


### Variance of a continuos Random Variable 

Definition 

$$
\text{Var}(X) = E[(X - \mu )^2] = E[X^2] - (E[X])^2
$$

therefore for a continuos variable, we have 

$$
\begin{aligned}
    \text{Var}(X) &= E[(X - \mu)^2] = \int _{-\infty} ^\infty (x - \mu x)^2 f_X(x) dx \\
    &= E[X^2] - (E[X])^2 = \int _{-\infty} ^\infty x^2 f_X(x) dx - \mu ^2 x
\end{aligned}
$$


also, we have 

$$
\text{Var}(aX + b) = a^2 \text{Var}(X)
$$


