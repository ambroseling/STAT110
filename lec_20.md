Find $E|z_1 - z_2| with z_1,z_2  $\sim$ N(0,I)$
- Note: $Z_1 - Z_2 \sim N(0,2)$
- $\sqrt{2} E|z| = \sqrt{2}\int_{-\infty}^{+\infty}|z|\frac{1}{\sqrt{2\pi}} e^{-\frac{z^2}{2}}dz = \sqrt{2}/ \pi$ 

Multinomial:
- hyperdimensional version of the binomial
- $Mult(n,\vec{p}), p = (p_1,...,p_k), p_{j} \gt 0, \Sigma_j p_j = 1$
- p is now a probability vector, all add up to 1
- in binomial case you have 2 categories (SUCCESS or FAILURE)
- in multinomial case, you have k categories
- $\vec{X} \sim Multi(n,\vec{p})$, $\vec{X} = (X_1,X_2,...,X_n)$ if have n objects, independently putting these n objects into k categories
- Joint PMF: $P(X_1=n_1, X_2=n_2, ..., X_n = ) = \frac{n!}{n_1!n_2!...n_k!} p_1^n_1 p_2^n_2 ... p_n^{n_k}$
    - what is the probability that there is $n_1$ objects in the first category, n_2 in the second category
    - we assume every objects belong to 1 category
- Marginal distribution of $X_j$:
    - $X_j \sim Bin(n,p_j)$
    - its either in category j or not
    - $E(X_j) = np_j $
    - $Var(X_j) = np_j (1-p_j)$
- Lumping property:
    - if we want to merge categories together
    - $\vec{X} = (X_1,X_2,X_3,...,X_10) \sim Mult(n,(p_1,...,p_10))$
    - Let $\vec{Y} = (X_1,X_2,X_3+...+X_10) \sim Mult(n,(p_1,p_2,p_3+...p_10))$

Conditional probability:
- $\vec{X} \sim Mult(n,\vec{p})$ Then given $X_1 = n_1$
- so we know how many people in X_1 category
- we want to find the rest
- $(X_2,...X_k) \sim Mult_{k-1}(n-n_1,(p_2',...,p_k'))$ with $p_2' = P(being in category 2 | not in category 1) = \frac{p_2}{1-p_1} = \frac{p_2}{p_2+...p_k}$
- $p_j' = \frac{p_j}{p_2 + ... + p_k}$

Cauchy Interview Problem
- the cauchy distribution of $\frac{X}{Y}$ with $X,Y \sim^{i.i.d} N(0,1)$
- does not have an expected value, no mean and variance
- you average a million cauchy's its still a cauchu distribution
- Find PDF of T:
- $P(\frac{X}{Y} \le t) = P(\frac{X}{Y} \le) = \int_{-\inf}^{+\inf} \int_{-\inf}^{t|y|}\frac{1}{\sqrt{2\pi}}e^{-x^2/2} dxdy$    
- $= \sqrt{\frac{2}{\pi}} \int_{0}^{\inf} e^{-y^2} \Phi(ty)dy$
- $= PDF:F'(t) = \sqrt{\frac{2}{\pi}} y*e^{\frac{-y^2}{2}} \frac{1}{\sqrt{2\pi}} e^{-t^2 y^2/2} \frac{1}{\pi} \int_{0}^{\inf} y e^{-(1+t)^2 y^2/2}dy$
- then use u-substituion $u = (1+t^2)y^2/2, du = (1+t^2)ydy$
- To get a probability you integrate over the region of interest
    - **symmetry of the normal


Theorem: X $\sim$ N(\mu_1,\sigma_1^2), Y \sim $N(\mu)$
indep 

$X + Y \sim N(\mu_1 + \mu_2 , \sigma_1^2 + \sigma_2^2)$

Proof:
- Use MGFs: MGF of X+Y is 
    - $e^{\mu_1t + 1/2 \sigma_1^2 t^2} * e^{\mu_2t + 1/2 \sigma_2^2 t^2} = e^{(\mu_1 + \mu_2)t + 1/2(\sigma_1^2 + \sigma_2^2)t^2}$
    