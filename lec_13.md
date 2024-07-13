Independence of r.v
- $X_1,X_2,...,X_n$
- Definition:
    - $X_1,X_2,...,X_n$ indep if $P(X_1 \leq x_1,..,X_n \leq x_n)$
    - $= P(X_1 \leq x_1) * P(X_2 \leq x_2) * P(X_n \leq X_n)$
    - Discrete case: (we call joint PMF)$P(X_1 = x_1,...,X_n = x_n) = P(X_1=x_1)P(X_2=x_2)...P(X_n=x_n)$

Ex:
- $X_1,X_2 \sim Bern(1/2) i.i.d$ , $X_3 = {1 \text{if} X_1=X_2, 0 \text{ptherwise}}$
- these are pairwise independent, not independent
- knowing $X_1$ and $X_2$ gives total information about $X_3$. 
- but knowing just $X_1$ and $X_2$ gives us nothing about $X_3$
Normal distribution

Normal Distribution
- central limit theorem: if you add a bunch of i.i.d random variables will look normal 
- $\mathcal{N}(0,1)$ has PDF $f(z) = c*e^{-z^2/2}$, $c$ is normalization constant 
    - 0 is mean
    - 1 is variance
- $\int_{-\infty}^{\infty} e^{-z^2/2} dz$, cant find antiderivative
- $\int_{-\infty}^{+\infty} e^{-z^2/2} dz \int_{-\infty}^{+\infty} e^{-z^2/2} dz  = \int_{-\infty}^{+\infty} e^{-x^2/2} dz \int_{-\infty}^{+\infty} e^{-y^2/2} dz $
- $\int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} e^{-(x^2+y^2)/2} dxdy = \int_{0}^{2 \pi} \int_{0}^{+\infty} e^{-r^2/2} r dr d\theta$
- $\int_{0}^{2\pi} (\int_{0}^{+\infty} e^{-u} dy) d \theta = 2 \pi$
- $\int_{-\infty}^{+\infty} e^{- z^2/2}dz = \sqrt{2\pi}$

Finding the mean (expected value):
- $E(Z) = \frac{1}{\sqrt{2\pi}} \int_{-infty}^{+infty} z e^{- z^2/2} dz = 0 by symmetry$
-  if $g(x)$ is an odd function (i.e. $g(-x) = g(x)$, then $\int_{-a}^{a} g(x)dx = 0$)

Variance:
- $Var(Z) = E(Z^2) - (EZ)^2 = E(Z^2)$
- $= \frac{1}{\sqrt{2 \pi}} \int_{-\infty}^{+\infty} z^2 e^{-z^2}/2 dz = \frac{2}{\sqrt{2\pi}} \int_{0}^{+\infty} z * z * e^{-z^2/2} dz$
- We use integration by parts:
    - $u = z$
    - $du = dz$
    - $dv = ze^{-z^2/2}$
    - $v = -e^{-z^2/2}$
- $= \frac{2}{\sqrt{2\pi}} ((uv)|_{0}^{\infty}+ \int_{0}^{+\infty} e^{-z^2/2}dz) = 1$
    - $(uv)|_{0}^{\infty}$ goes to 1
    - $\int_{0}^{+\infty} e^{-z^2/2}dz$ becomes $\frac{\sqrt{2\pi}}{2}$
    
