Standard normal:
- $z \sim \mathcal{N}(0,1)$
- CDF: $\phi$
- $E(Z) = 0$
- Var(Z) = E(Z^2) = 1

Let $X = \mu + \sigma z$
- $\mu \in R$ (mean,location)
- $\sigma \gt 0$ (SD, scale)
- we get $X \sim \mathcal{N(\mu,\sigma^2)}$
- $E(X) = \mu$
- $Var(X) = E((X-(EX)^2)) = EX^2 - (EX)^2$
- $Var(X+c) = Var(x)$ 
- $Var(cx) = c^2 Var(x)$
    - remember to square the constant
- $Var(X) \gt 0$, $Var(X)=0$
    - if and only if $P(X=a) = 1$ for some $a$
- In general, $Var(X+Y) \neq Var(X) + Var(Y)$ [only if X,Y are independent]
- $Var(X+X) = Var(2X) = 4 Var(X)$
    - if $X_1$ and $X_2$ are indepent, the variability would just add

Standardization:
- $z = \frac{x - \mu}{\sigma}$

Find PDF of $N(\mu,\sigma^2)$
- CDF: $P(X \leq x)= P(\frac{X - \mu}{\sigma} \leq \frac{x - \mu}{\sigma}) = \Phi(\frac{x - \mu}{\sigma})$
- Just evaluate the standard normal PDF at $\frac{1}{\sigma \sqrt{2\pi}} e^{-(\frac{x-\mu}{\sigma})^2/2}$
- $-X = -\mu + \sigma(-Z) \sim \mathcal{-\mu, \sigma^2}$

- If $X_j \sim \mathcal{N}(\mu_j,\sigma_j^2) are independent$, $X_1 + X_2 \sim \mathcal{N}(\mu_1 + \mu_2, \sigma_1^2 + \sigma_2^2)$
- $X_1,X_2 \sim \mathcal{N}(\mu_1 + \mu_2, \sigma_1^2 + \sigma_2^2)$


68-95-99.7 Rule
- if $X \sim \mathcal{N}(\mu,\sigma^2)$ is normal
- $P(|x-\mu| \leq \sigma) \approx 0.68$
- $P(|x-\mu | \leq 2 \sigma) \approx 0.95$
- $P(|x - \mu | \leq 3 \sigma) \approx= 0.997$

LOTUS:
- $PMF: P_0,P_1,P_2,P_3$
- $X: 0,1,2,3...$
- $X^2: 0^2,1^2,2^2,3^2$
- $E(X) = \Sigma_x x P(X = x)$
- $E(X^2) = \Sigma_x x^2 P(X = x)$


We want to find variance of Poisson, applying LOTUS on the Poisson to find $E(X^2)$: 
- $E(X^2) = \Sigma_{k=0}^{\infty} k^2 \frac{e^{-\lambda}\lambda^k}{k!}$
- Start with what we know:
    - $\Sigma_{k=0}^{\infty} \frac{\lambda^k}{k!} = e^{\lambda}$
    - $\lambda* \Sigma_{k=1}^{\infty} \frac{k \lambda^{k-1}}{k!} = \lambda e^{\lambda}$
    - $\Sigma_{k=1}^{\infty} \frac{k \lambda^k}{k!} = \lambda e^{\lambda}$
    - $\Sigma_{k=1}^{\infty} \frac{k^2\lambda^{k-1}}{k!} = e^{lambda} (\lambda +1)$
- $Var(X) = \lambda^2 + \lambda - \lambda^2 = \lambda$

Find $X \sim Bin(n,p), Find Var(X)$
- $X = I_1 + ... I_n, I_j \sim i.i.d Bern(p)$
- $X^2 = I_1^2+...+I_n^2 + 2I_1*I_2 + 2I_1*I_3 + ... + 2I_{n-1}I_{n} $
- $E(X^2)=n E(I_1^2) + 2 {n \choose 2} E(I_1 I_2)$
- $E(X^2) = np + n (n-1) p^2 = np + n^2p^2 -np^2$
- $Var(X) = np - np^2 = np(1-p) = npq$

Prove LOTUS for discrete sample space (pebble world):
- Show $E(g(x)) = \Sigma_{\lambda} g(x) P(X = x) $
- $\Sigma_{x} g(x)P(X=x) = \Sigma_{s \in S} g(X(s)) P({s})$
- left is grouped
- right is ungrouped