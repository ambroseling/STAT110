# Random Vairables and Distributions

# Gamblers Ruin Problem
- 2 gamblers, one goes bankrupt 
- sequence of rounds where they bet $1, p = P(A wins a certain round)
 - q = 1 - p: B wins

 Find the probabiliyt that A wins entire game (so B is bankrupt)
 - Assume A starts with $i dollars and B starts with $(N-i)
 - Random walk: |0----i------N|, p = prob of going right
 - Strategy: condition on first step
    - Let $p_i = P(A wins game | starts with i dollars)$
    - $p_i = p * p_{i+1} + q * p_{i-1}$ - difference equation
$$
p_i = p * p_{i+1} + q * p_{i-1} \\
$$

Guess: $p_i = x^i$
$$
x^i = p * x^{i+1} + q * x^{i-1} \\
p * x^2 - x + q = 0 \\
x =  \frac{1 +- \sqrt{1 - 4pq}}{2p} \in \{ 1, \frac{2 - 2p}{2p} = \frac{q}{p}\}
$$

So the general form is :
$$
p_i = A*1^i + B(\frac{q}{p})^i \\
p_0 = 0 \rightarrow B = -A, p_N = 1 \rightarrow 1 = A(1 - \frac{q}{p})^N
$$


Difference equation :
$$
p_i = \{ \frac{1 - (q/p)^i}{ 1 - (q/p)^N}\} if p \neq q \\
p_i = \{i /N\} , if p = q \\

$$ 

You can take the limit of the unfair case and see it converges to the fair case as lim x->

## What is a random variable?
- It is a function from a sample space S to R 
- Input is some possible outcome $S_0$ to the real line
- Think of as a numerical summary of an aspect of the experiment
- where does the randomness come from?
    - the randomness of the experiment

## Definition of Bernouli
- A random variable X is said to have Bern distribution if X only has 2 possible values 0 and 1, and P(x=1) = p , P(x = 0) = 1 - p
- X = 1 is an event

## Definition of Binomial 
- the distribution of # of successes in n independent Bern(p) trials is called Bin (n,p)
- its distribution is given by : $P(x =k) = {n \choose k} p^k (1 -p)^{n-k}$
- 1 1 1 0 0 0 0  
- n = 7, k = 3
- **NOTE**: we choose where the successes are hence n choose k, we have k successes out of n trials.