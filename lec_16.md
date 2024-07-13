Exponential distribution
- one parameter $\lambda$ or rate parameter or the rate at which sth occurs
- $X \sim Exp(\lambda)$ has PDF $\lambda^{-\lambda x}, x \gt 0 (\text{0 otherwise})$
- CDF $F(X) = \int_{0}^{x} \lambda e^{-\lambda*t}dt = 1 - e^{-\lambda x}, x \gt 0$
- Let $Y = \lambda X$, then $Y \sim Expo(1)$ since $P(Y \leq y) = P(X \leq \frac{y}{\lambda}) = 1 - e^{-y}$

- Finding the mean and variance
    - find $E(Y)$ and $Var(Y)$, we use integration by parts
    - $E(Y) = \int_{0}^{\infty} y e^{-y} dy = (-y e^{-y})|_{0}^{\infty} + \int_{0}^{\infty} e^{-y} dy = 1$ 
        - where $du = dy$ and $v = e^{-y}$
        - the $(-y e^{-y})|_{0}^{\infty} $ term is just 0, so expected value is just 1
    - Variance:
        - $Var(Y) = E(Y^2) - (EY)^2 = \int_{0}^{\infty} y^2 e^{-y} dy - 1 = 1$


- So $X = \frac{Y}{\lambda} $ has $E(Xs) = \frac{1}{\lambda}$, $Var(X) = \frac{1}{\lambda^2}$
- Exponential distribution has a **memoryless** property
    - $P(X \gt s+t | X \geq s) = P(X \geq t)$
    - this means that you already waited for s minutes, what is the probability that you have to wait for an additional t minutes, it is the same as $P(X \geq t)$, because you start fresh with a new parameter t
    - Here $P(X \gt s) = 1 - P(X \leq s) = e^{-\lambda * s}$, we just use definition of conditional probability:
    - $P(X \geq s + t | X \geq s) = \frac{P(X \geq s + t, X \geq s)}{P(X \geq s)} = \frac{e^{-\lambda(s+t)}}{e^{-\lambda s}} = e^{-\lambda t} = P(X \geq t)$
    - How to use memoryless property?
        - $E(X|X \gt a) = a + \frac{1}{\lambda} by memoryless property$
    - Theorem: 
        - if $X$ is a + continous r.v. with memory less property (r.v. is memoryless if distribution is memoryless) , it has to be $X \sim Expo(\lambda)$ for some $\lambda$
        -  Proof:
            - Let $F$ be the CDF of $X$, $G(x) = P(X \gt x) = 1 - F(x)$
            - Memory property is $G(s+t) = G(s)G(t)$
            - $s = t \rightarrow G(2t) = G(t)^2, G(3t) = G(t)^3,...,G(kt) = G(t)^k$
            - $G(t/2) = G(t)^{-1/2}, G(t/3) = G(t)^{1/3} $
            - $G(\frac{m}{n}t) = G(t)^{m/n}$, so $G(xt) = G(t)^x$
            - Let t = 1, $G(x) = G(1)^{x} = e^{}$