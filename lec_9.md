CDFs:
- $F(x)= P(X \leq x)$, as a function of real X
- discrete:
    - looks like a step function
    - the jump sizes are the PDFs
    - Find $P(1 \leq X \leq 3)$:
        - $P(X \leq 1) + P(1 \leq X \leq 3) = P(X \leq 3)$
        - $\rightarrow P(1 \lt X \leq 3) = F(3) - F(1)$
        - careful of the inequality
        - $P(a \lt X \leq b) = F(b) - F(a)$
- Properties of CDF:
    - increasing
    - right continous
    - as $X$ goes to -inf , $F(x) \rightarrow 0$
    - **NOTE**: THis is if and only if, CDF must satisfy these 3 things

- Indep of r.v.s:
    - X,Y are indep r.v.s. if $P(X \leq x, Y \leq y) = P(X \leq x) P(Y \leq y) for all x,y$
    - Discrete case:
        - $P(X = x,Y=y) = P(X = x)P(Y = y)$
        - **NOTE**: intuitively just means knowing the value of X tells you nothing about the value of Y

Averages
- would assume the means, expected value
- one number summary of a distribution, but can be very useful
- 1,2,3,4,5,6 $\rightarrow$ 
- $\frac{1}{n} \Sigma_{j=1}^{n} j = (n+1)/2$
- 1,1,1,1,1,3,3,5
    - 2 ways to compute average:
        - add everything divide by 8
        - weighted average: $\frac{5}{8} * 1  + \frac{2}{8} * 3 + \frac{1}{8} * 5$
- Average of a discrete r.v. of X:
    - $E(x) = \Sigma_{x} x * PMF(x)$
- Bernouli Example:
    - x ~ Bernouli(p)
    - $E(x) = 1* P(X =1) + 0 * P(X=0) = P$
    - $X = \{E(X) = P(A)\}$
- Binomial Example:
    $$ 
    E(x) = \Sigma_{k=0}^{n} k * {n \choose k} p^k q_{n-k} \\
    E(x) =  \Sigma_{k=1}^{n} {n-1 \choose k-1} p^k q^{n-k} \\ 
    E(x)  = n*p \Sigma_{k=1}^{n} {n-1 \choose k-1} p^{k-1} q^{n-k}
    E(x)  = n*p \Sigma_{k=1}^{n} {n-1 \choose k-1} p^{k-1}q^{n-k}
    E(x) = n*p \Sigma_{j=0}^{n-j} {n-1 \choose j} p^j q^{n-1-j}  
    $$

- Linearity
    - $E(X+Y)  = E(x) + E(Y)$
    - even if X and Y are dependent
    - $E(c*X) = c * E(X)$
    - if c is a constant

- Redo Binomial Example:
    - By linearity if you have $n*p$ 
    - Since $X = X_1 + X_2 + ... + X_n$
    - $X_j \sim Bern(p)$


- Another example (hyper geometric distribution)
    - 5 card hand, X = (# of aces)
    - Let $X_i$ be indicator of jth card
    - $E(X) = E(X_1 + ... + X_5) = E(X_1) + ... + E(X_5) = 5 P(\text{1st card is an ace}) = 5/13$, even though the $X_j's$ are dependent
    - This gives of expected value of any hypergeometric distribution (trials are dependent, but expected value is just n times the probability of first case)

- Another Famous distribution (geometric distribution)
    - Geom(p): independent bernouli p trias
    - count number of failures before 1st success
    - Sequence: F F F F F S
    - $PMF: P(X = k) = q^k * p , k \in \{0,1,2,...\}$
    - It is valid since $\Sigma_{k=0}^{\infty} pq^k = \frac{p}{1-q} = 1$

- $X \sim Geom(p)$
    - $E(x) = \Sigma_{k=0}^{\infty} k * p * q^k$
    - $E(X) = p \Sigma_{k=1}^{\infty} k * q^k$
    - this is very hard to work with a $k$ in front, lets use what we know
    - $\Sigma_{k=0}^{\infty} q^k = \frac{1}{1-q}$
    - $\Sigma_{k=1}^{\infty}k*q^{k-1} = \frac{1}{(1-q)^2}$
    - $\Sigma_{k=1}^{\infty}  = \frac{q}{p^2}$
    - now we know that $\Sigma_{k=1}^{\infty}  = \frac{q}{p^2}$, we can replace it where we left off in the expected value calculation
    - $E(X) = p \Sigma_{k=1}^{\infty} k * q^k$
    - $E(X) = \frac{p*q}{p^2} = \frac{q}{p}$
- Story proof for $X \sim Geom(p)$
    - Let $c = E(X)$
        - $c = 0 * p + (1+c) *q$
            - Either we have a success, land with heads, happens with probabiltiy p
            - if its failure again, 1 failure then problem restarts, +c again
        - $c = q + c*q$
        - we isolate for c
        - $c = q / p$ 
