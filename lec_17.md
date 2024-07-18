Moment Generating Functions 
- Definition: A r.v. has MGF $M(t) = E(e^{tX})$ as a function of t, if it is finite on some interval [-a,a], a > 0
- Why its moment generating?
    - $E(e^{tX}) = E(\Sigma_{n=0}^{\infty} \frac{x^n t^n}{n!}) = \Sigma_{0}^{\infty} \frac{E(x^n)t^n}{n!}$
- Why moments are importnant:
    - the nth moment $E(x^n)$ is coef of $\frac{t^n}{n!}$ in Taylor Series expansion in MGF M(t)
    - MGF determines distribution, if X and Y have same MGF they have same distribution
    - if X has MGF $M_x$ and Y has MGF $M_y$ , X independent of Y, then MGF of $X+Y = E(e^{t(X+Y)}) = E(e^{tX})*E(e^{tY}) = M_x(t) * M_y(t)$
    - Ex. $X \sim Bern(p) \rightarrow M(t) = E(e^{tx})= pe^{t} + q = pe^{t} + (1-p)$
    - $X \sim Bin(n,p) \rightarrow M(t) = (pe^t + q)^n$
    - Ex with standard normal:
        - $Z \sim \mathcal{N}(0,1) \rightarrow M(t) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty} e^{tz - \frac{z^2}{2}} dz$
        - Linear term is annoying, find ways to get rid of it
        - $= \frac{e^{t^2/2}}{\sqrt{2}{\pi}} \int_{-\infty}^{+\infty} e^{-\frac{1}{2} (z-t)^2} dz$
        - key here is recognizing the integral is same as just integrating standard normal with distribution centered at t
        - so integral goes to 1, $=e^{t^2/2} $


Laplace's rule of succession
- whats the probability the sun will rise tomorrow?
- Given p, $X_1,X_2,X_3,...$ i.i.d. Bern(p) , $\rightarrow$ 
- p is unknown, Bayesian: treat p as r.v.
- Let $p \sim Unif(0,1)$ (prior), let $S_n = X_1 + X_2 + X_3...X_n$
- $S_n|p \sim Bin(n,p), p \sim Unif(0,1)$ 
- Find posterior $p|S_n$ (we observed $S_n$), and $P(X_{n+1}=1= | S_n = n)$
- $f(p|S_n = k)$ - conditional pdf, we can still apply bayes rule, p is a random variable in thise case
- $f(p|S_n = k) = \frac{P(S_n = k|p)f(p)}{P(S_n = k)}$
    - we can use law of total probability: $P(S_n = k)$ which we know does not depend on lowercase p
    - $P(S_n = k) = \int_{0}^{1} P(S_n = k|p) f(p) dp$
- $f(p|S_n = k)$ is proportional to $P(S_n =k | p) = p^k (1-p)^{n-k}$:
    - numerator: $P(S_n =k | p) = p^k (1-p)^{n-k}$
- for the case where the sun did rise of the last n days:
    - $P(X_{n+1}=1|S_n = n) = \int_{0}^{1} (n+1)p p^m dp = \frac{n+1}{n+2}$