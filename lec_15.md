Coupon collector (toy collector)
- kind of like Mcdonalds toys, how long does it take on average to collect the full set
- n toy types, equally likely
- Find expected time  (number of toys) until you have complete set:
    - $T_1 = $ time until you get 1st new toy $=1$
    - $T_2 = $ additional time until $2nd$ new toy
    - $T_3 = $ additional time until $3rd$ new toy
    - $T_1 = 1, T_2 - 1 \sim Geom(\frac{n - 1}{n})$
        - there are n different toy types
        - we already have 1 of the n
        - (n-1)/n chances that you'll get a new toy 
    - $T_j - 1 \sim Geom(\frac{n - (j-1)}{n})$
    - $E(T) = E(T_1) + E(T_2) + ... E(T_n)$
    - $E(T) = 1 + \frac{n}{n-1} + \frac{n}{n-2} + ... + \frac{n}{1} = n(1 + \frac{1}{2} + \frac{1}{3} + ... + \frac{1}{n})$

Universality:
- F is CDF
- $X \sim F$
- We pick a random value on the x axis we call $x_0$
- Lets say we know that $F(x_0) = \frac{1}{3}$
- We want to find what is the probality that:
    - $P(F(X) \leq \frac{1}{3}) = P(X \leq x_0) = F(x_0) = \frac{1}{3}$
    - $F(X) \sim Unif(0,1)$
- Logistic regression:
    - $F(X) = \frac{e^x}{1+e^x}$
    - $U \sim Unif(0,1), consider$
    - $F^-1(u) = log(\frac{u}{1 - u})$


Another 
- NOTE: Linearity is for SUMS
- Let X,Y,Z be i.i.d (independent, identically distributed) be positive r.v.s.
- Find $E(\frac{X}{X + Y + Z})$
    - Find $E(\frac{X}{X+Y+Z}) = E(\frac{Y}{X+Y+Z}) = E(\frac{Z}{X+Y+Z})$
    - why? just by symmetry since they are iid
    - $E(\frac{X}{X+Y+Z}) + E(\frac{Y}{X+Y+Z}) + E(\frac{Z}{X+Y+Z}) = E(\frac{X+Y+Z}{X+Y+Z}) = 1$
    - $E(\frac{X}{X+Y+Z}) = \frac{1}{3}$


LOTUS:
- Given that $U \sim Uniform(0,1), X = U^2, Y = e^X$
- Find $E(Y) as an integral$:
    - Approach 1: 
        - $E(Y) = \int_{0}^{1} e^x f(x)dx$
            - $e^x$ is the PDF of the Y
            - Find CDF:
                -  $P(U^2 \leq X) = P(U \leq \sqrt{x}) = \sqrt{x}$ if $0 \lt x \lt 1$
                - $f(x) = (1/2) x^{-1/2}$
        - so you can find CDF then take derivative to get PDF and sub it in
        - but this is more work
    - Approach 2:
        - $E(Y) = \int_{0}^{1} e^{u^2} du$


Story proof:
- $X \sim Bin(n,p), q = 1 - p$
- Find distribution of n - X
    - Approach 1: proof with PMF
        - $P(n - X = k) = P(X = n-k)$
        - ${n \choose n-k} p^{n-k}q^{k} = {n \choose k} q^{k}p^{n-k}$ 
    - Approach 2: story proof:
        - its the same as swapping successes with failures
        - $n - X \sim Bin(n-q)$


Poisson problem:
- num of emails in a time interval t is Pois(\lambda * t)
- find PDF fo T, time of 1st email
- $P(T \gt t) = P(N_t = 0)$ with $N_t = (\text{# emails in} [0,t])$
- $P(N_t = 0) = e^{-\lambda * t} (\lambda * t)^0 / 0! = e^{-\lambda * t}$
- CDF is $1 - e^{-\lambda * t}, t \gt 0$