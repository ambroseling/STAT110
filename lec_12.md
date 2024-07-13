Discrete
- PMF: P(X = x)
- CDF: $F_x(x) = P(X \leq x)$
- E(X) = $\Sigma_x xP(X = x)$
- Var(X) = E(X^2) - (EX)^2
- LOTUS: $E g(X) = \Sigma_x g(x) P(X = x)$

Continous
- PDF $f_x(x) = F'_x(x) [P(X = x) = 0]$
- CDF: $F_x(x) = P(X \leq x)$
- Expected value: $E(X) = \int_{-\infty}^{+\infty} x f(x) dx$
- LOTUS: 

Variance:
- $ Var(X) = E(X - EX)^2$
- Standard deviation: $SD(X)  = \sqrt{Var(X)}$

Another way to express Var:
- $Var(X) = E(x^2 - 2X(EX) + (EX)^2) = E(X^2) - E(X)E(X) + (EX)^2$
- $Var(X) = E(X^2) - (EX)^2$

Continous distributions
- cant use pebbles anymore, 
- PDF (probability density function): $$
    - Def: R.V. $X$ has PDF $f(x)$ if $P(a \leq X \leq b) = \int_a^b f(x)dx$ for all a and b
    - To be valid, $f(x) \geq 0$ and $\int_{-\infty}^{\infty} f(x)dx = 1$
    - $f(x_0) \epsilon \approx P(X \in (x_0 - \frac{\epsilon}{2} , x_0 + \frac{\epsilon}{2}))$ for $\epsilon \geq 0$ very small
- CDF: 
    - If X has PDF $f$, the CDF is $F(X) = P(X \leq x) = \int_{-\infty}^{x} f(x)dt$
    - If X has CDF $F$ (and X is continous) then $f(x) = F'(x)$, we assume $F'(X)$
    - $P(a \leq x leq b) = \int_{a}^{b} f(x) dx = F(b) - F(a)$


Uniform distribition: (uniform is universal)
- some interval from a to b, pick a random point in this interval $[a,b]$
- Unif: probability is **proportional** to length
- $f(x) = $
    - $c ,$ if $a \leq x \leq b$
    - 0 otherwise
- $1 = \int_{a}^{b} c dx= c = \frac{1}{b-a}$
- CDF: $F(x) = \frac{-\infty}{x} f(x)dx =  \int_{a}^{x} f(t)dt$
    - 0 if $x \lt a$
    - $\frac{x-a}{b-a}$, if $a \leq x \leq b$
    - 1 if $x \gt b$
- E(x) = $\int_{a}^{b} \frac{x}{b-a} dx = \frac{x^2}{2(b-a)}|_{a}^b$
- E(x) = $(a+b)/2$
- Variance:
    - $E(X^2) = E(Y) = \int_{-\infty}^{+\infty} x^2 f(x)dx$
    - Law of the unconscious statistician:
        - $E(g(x)) = \int_{-infty}^{+infty} g(x) f_x(x)dx$
        - Example:
            - $E(u) = \frac{1}{2}$
            - $E(u^2) = \int_{0}^{1} u^2 f(u)du$
            - $Var(u) = E(u^2) - (Eu)^2$
- Uniform is universal
    - Let $U \sim Unif(0,1), F be a CDF (assume F is strictly increasing and contionus)$
    - Theorem: Let $X = F^-1(u)$ Then $X \sim F$
    - Proof:
        - $P(X \leq x) = P(F^-1(u) \leq x) = P(U \leq F(x)) = F(x)$
        - NOTE: 
            - U is a probability from 0 to 1
            - probability is proportional to length
            - whole interval is 1
    - Also if $X \sim F$, then $F(X) \sim Unif(0,1) $, then $F(X) \sim Unif(0,1)$
    - Ex. $F(x) = 1 - e^{-x}$
    - Ex. Let $F(x) = 1 - e^{-x}, x > 0 (Exp(1)), U \sim Unif(0,1)$
        - Simulate $X \sim F$
            - $F^{-1}(u) = -ln(1-u) \rightarrow F^-1(u) = -ln(1-u) = F$
            - $1 - U \sim Unif(0,1) (Symmetry of Unif)$
            - 

