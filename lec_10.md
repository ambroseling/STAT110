Expectation continued

Let T = X+Y, show that $E(T) = E(X) + E(Y)$
- Apply the defintion
- $\Sigma_{t} t * P(T = t)  = \Sigma_{x} x * P(X = x) + \Sigma_{y} y * P(Y = y)$

- we apply pebble example:
- $E(X) = \Sigma_{x}^{} x*P(X = x) = \Sigma_{s} X(s) P(\{s\})$
- left one is **grouped**, right one is **ungrouped**

- Proof of linearity
    - $E(T) = \Sigma_{s} (X+Y)(s) P(\{s\}) = \Sigma_{s} (X(s) + Y(s)) P(\{s\})$
    - $E(T) = \Sigma_{s} (X+Y)(s)P(\{s\}) = \Sigma_{s}X(s) + \Sigma_{}Y(s)P(\{s\}) = E(X) + E(Y)$
    - $E(T) = E(X) + E(Y)$

- Similarily, $E(cX) = c E(x)$ if $c$ is a constant
- Extreme case of dependence: $X = Y$
    - $E(X+Y) = E(2x) = E(X) + E(Y)$

- Negative binomial: parameters r and p
    - Story: independent Bern(p) trials # of failures before the rth success
    - PMF:
        - 1 0 0 0 1 0 0 1 0 0 0 0 0 1 0 0 1
        - r = 5, n = 11
        - when you stop it has to be a success
        - it doesnt matter if you permute the order of the 1s or 0s before the rth success
        - $P(X = n) = {n+r-1 \choose r-1} p^r (1-p)^n$ for n = 0,1,2,3...
    - $E(X) = E(X_1 + X_2 + ... + X_r) = E(X_1) + ... + E(X_r) = \frac{r*q}{p}$
        - think of as wait for 1st sucess then the 2nd
        - $X_j$ is # of failures btw $(j-1)st$ and jth success; $X_j \sim Geom(p)$
    -  $X \sim FS(p) time until 1st success,counting the success$
        - Let $Y = X - 1$. Then $Y \sim Geom(p)$
        - $E(X) = E(Y) + 1 = \frac{q}{p} + 1 = \frac{1}{p}$

- Random permutation 1,2,...n. where n >=2 
    - find expected # of local maxima within a sequence of numbers
    - Let $I_j$ be the indicator r.v. of position j having a local max, $1 \leq j \leq n$
    - 3 2 1 4 7 5 6
        - 
    - $E(X) = E(X_1) + ... +E(X_n)  = \frac{n+2}{2} + \frac{2}{2} = \frac{n+1}{3}$ 
- St Petersburg Paradox
    - Get $\$2^x$ , where X is # of flips of fair coin until first H, including the success
    -  $Y = 2^X, find $E(Y)$$
    - Assyming we have infinite amount of money:
        - $E(Y) = \Sigma_{k=1}^{\infty} 2^k * \frac{1}{2^k}= \Sigma_{k=1}^{\infty} 1 = \infty$
    - But in the real world, nobody has infinite amount of money, we assume to impose an upper bound
        - we set a bound at $2^40$ dollars
        - Then $\Sigma_{k=1}^{40} 2^k * \frac{1}{2^k} = 40$
        

