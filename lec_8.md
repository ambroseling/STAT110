# Binomial distribution: 
- Bin(n,p)
- n is any positive integer
- p is any real number btw 0 and 1

- Story: 
    - X is the # of successes in n independent Bern(p) trials
- Indicator r.v.s:
    - $X = X_1 + X_2 + ... + X_n$
    - $X_j = \{1   \text{if jth trial is success}; 0   \text{otherwise}\}$
    - $X_i,...,X_n$ i.i.d. Bern(p)
    - $P(X = k) = {n \choose k} p^k q^{n-k} = (p+q)^n = 1$
- PMF (discrete r.v.s):
    - $P(X=k) = (n \choose k) p ^ k q (1-p)^{n-k}$
    - discrete: possible values $a_1,a_2,a_3,...a_n$ discrete integers
    - PMF is just the probability that $P(X = a_j)$ for all j
        - we also require that $p_j \geq 0, \Sigma_j p_j = 1$
- R.V.S:
    - we assign a number to each pebble in the pebbles (possible outcomes) in our sample space
    - X = 7 is an event
    - CDF:
        - $X  \leq x$ is an event
        - $F(X) = P(X \leq x)$
        - then F is the CDF of x (cummulative distribution function)

$X \sim Bin(n,p) , Y \sim Bin(m,p) \rightarrow X+Y \sim Bin(n+m,p)$
- Intuition, you flip a coin n times and indepedently 
- number of successes is just successes from first experiment with the successes of the second experiment, just add them together
- we need to assume that the trails are independent, has the same proability 

Let X = # of aces (event mapped to an integer 0-4):
- This is NOT a bernouli trail, when you draw an aceit affects the probability of the next trail, not independent
- $P(X = ) = \frac{{4 \choose k}{ 48 \choose 5-k}}{{52 \choose 5}}$ for $k \in \{0,1,2,3,4\}$
- Vandermont: $$
- Distribution is not a binomial
- Trails are not independent
- Story for the hypergoemtric distribution: 
    - Jar full of marbles, have $b$ black marbles, $w$ white marbles. Pick simple random sample of $n$. Find dist of # white marbles in sample:
    - $P(X = k) = \frac{{w \choose k}{b \choose n-k}}{{w+b \choose n}}, 0 \leq k \leq w, 0 \leq n-k \leq b$
    - key is that sampling without replacement, trials are not independent
    - Check that its a PMF:
        - $\Simga_{k=0}^{W} \frac{{W \choose k}{b \choose n-k}}{{w+b \choose n}}$

- CDF:
    - continous: contious curve like a tanh
    - discrete: has jumps discontinous
