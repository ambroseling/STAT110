The Poisson Distribution

Sympathetic Magic
- dont confuse at e.v. with its distribution
- r.v. is the house
- distribition is the blueprint of the house


Poisson Distribution
- PMF: $P(X=k) = e^{-\lambda} \frac{\lambda^k}{k!}$, $k \in \{0,1,2,3...\}$
    - $\lambda$ is the rate parameter
- check that its a valid PMF:
    - $\Sigma_{k=0}^{\infty} \frac{e^{-\lambda}\lambda^k}{k!} = e^{-\lambda} e^{lambda} = 1$
    - $E(X) = e^{-\lambda} \Sigma_{k=0}^{\infty} k * \frac{\lambda^k}{k!}$
    - $E(X) = \lambda e^{-\lambda} \Sigma_{k=1}^{\infty} \frac{\lambda^{k-1}}{(k-1)!} = \lambda e^{-\lambda} e^{lambda} = \lambda$
- Application:
    - often used for counting # of successes where ther are a large number of trials, each with small prob of success
    - \# of emails in an hour
    - \# of chips in a chocolate chip cookie
    - \# of earthquakes in a year in a given region

Poisson Paradigm (approximation)
- Events $A_1,A_2,...,A_n$
- $P(A_j) = p_j$, $n$ is large but $p_j$ is small
- could be with weak independence
- \# of $A_j$'s that occur is approx Pois($\lambda$)
- $\lambda = \Sigma_{j=1}^{n} p_j$  

Connection to Binomial ($X \sim Bin(n,p)$)
- let $n \rightarrow \infty$ , $p \rightarrow 0$, we take the limit and see how it converges of Binomial to Poisson
- $\lambda = n*p , p = \frac{\lambda}{n}$
- Find what happens to $P(X = k)$
- $P(X = k) = {n \choose k} p^k (1-p)^{n-k}$, k is fixed
- $P(X = k) = \frac{n*(n-1)*...*(n-k+1)}{k! n^k} (1- \frac{\lambda}{n})^k (1-\frac{\lambda}{n})^{-k}$
    - $({\lambda}{n})^{-k}$ goes to 1
    - $(1- \frac{\lambda}{n})^k$ goes to $e^{-\lambda}$
    - From $\frac{n*(n-1)*...*(n-k+1)}{k! n^k}$ we can take out $\frac{\lambda^k}{k!} and the rest goes to 1$

Birthday problem (triple birthday matches)
- Have $n$ people, find approx prob that 3 epople with same birthday
- ${n \choose 3}$ triplets of people 
- Indicator r.v. for each $I_{i,j,k}$, $i \leq j \leq k$
- $E(\text{number of triplet matches}) = {n \choose 3} \frac{1}{365^2}$
- X = # of triple matches approx Pois($\lambda$) , $\lambda = {n \choose 3} \frac{1}{365^2}$
- We want to find the probability of at least 1 triple match
- $P(X \geq 1) = 1 - P(X = 0) \approx 1 - \frac{e^{-\lambda} \lambda^0}{0!} = 1 - e^{- \lambda}$


