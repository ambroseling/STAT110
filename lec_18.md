Exponential MGF  
- $X \sim Expo(1)$, find the MGF (moments), find moments using lotus: $M(t) = E(e^{tx}) = \int_{0}^{\infty} e^{-x} dx = \int_{0}^{\infty} e^{-x(1-t)}dx = \frac{1}{1-t}, t \lt 1$
- $M'(0) = E(X), M''(0) = E(X^2), M'''(0) = E(X)^3$
- $\frac{1}{1-t} = \Sigma_{n=0}^{\infty} t^n = \Sigma_{\infty}^{n=0} n! \frac{t^n}{n!} = E(X^n) = n!$
- then let $Y \sim Expo(\lambda)$, let $X = \lambda Y \sim Expo(1)$, so $Y^n = \frac{X^n}{\lambda^n}$


Let $Z \sim \mathcal{0,1}, find all the moments:$
- $E(Z^n) = 0$ for n odd by symmetry
- MGF: $M(t) = e^{t^2/2} = \Sigma_{n=0}^{\infty} \frac{(t^2/2)^n}{n!} = \Sigma_{n=0}^{\infty} \frac{t^{2n}}{2^n n!}$
- $\rightarrow E(Z^{2n}) = \frac{(2n)!}{2^n n!}$


Poisson MGF:
- $X \sim Pois(\lambda) $
- $E(e^{tx}) = \Sigma_{k=0}^{\infty} e^{tk} e^{-\lambda} \frac{\lambda^k}{k!}$
- then recognize its just the taylor series for e evaluated at $\lambda e^t$
- $= e^{-\lambda}e^{\lambda e^{t}} = e^{\lambda (e^t - 1)}$
- Multiply MGFs:
    - Ex. Let $Y \sim Pois(\mu)$ independent of X. Find the distribution of $X+Y$, so you can multiply MGFs:
        - $e^{\lambda(e^t - 1)} e^{\mu (e^t -1)} = e^{(\lambda + \mu)(e^t - 1)} \rightarrow X + Y \sim Pois(\lambda+\mu)$
        - this is only true if $X$ independent of $Y$, if it were dependent where Y = X
        - it is no longer Poisson, $X + Y = 2X$ is not Poisson since it is even
        - $E(X) = 2\lambda, Var(2X) = 4 \lambda$


Joint Distributions
- $X,Y$ Bernouli

|      | Y = 0  | Y = 1|
|------|------|----------|
|X = 0 | 2/6  |   1/6   |
|X = 1 | 2/6  |    1/6|

- Marginal for X: $P(X=0) = 3/6$, $P(X=1) = 3/6$ 
- Marginal for Y: $P(Y=0) = 4/6, P(Y=1) = 3/6$
- We can check they are independent if the marginals mutliply to make the entry (3/6 * 4/6)
- 

- $X,Y$ r.v.s 
    - Joint CDF: $F(x,y) = P(X \leq x, Y \leq y)$
    - Joint PDF: $P((X,Y) \in B) = \int\int_{B} f(x,y)dxdy$
    - Joint PMF (discrete case): $P(X = x, Y = y) $
    - Marginal CDF: $P(X \lt x)$ is marginal distribution of X
    - Independence:
        - X,Y indep if and only if $F(X,Y) = F(X) F(Y)$

Ex. Uniform on square ${(x,y): x,y \in [0,1]}$
- Joint PDF: constant on the square
- $= {c , 0 \leq x \leq 1}, o \text{otherwise}$
- integral is area, c = 1/area = 1

Ex. Uniform on circle $x^2 + y^2 \lt 1$
- Joint PDF: ${\frac{1}{\pi}} , x^2 + y^2 = 1$
- X,Y dependent because of the constraint
- Given X = x, $-\sqrt{1 - x^2} \leq y \leq \sqrt{1 - x^2}$