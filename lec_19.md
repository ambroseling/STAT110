Joint, Conditional, Marginal dist:
- Joint CDF: $F(x,y) = P(X \lt x, Y \lt y)$
- continous case joint PDF:
    - $f(x,y) = \frac{\partial}{\partial{x} \partial{y}}$
    - $P((x,y) \in A ) = \int\int_A f(x,y) dxdy$
- Marginal PDF of X: $\int_{-\infty}^{\infty} f(x,y)dy$, integrate out the y
- Double integral: $\int\intf(x,y)dxdy = 1$

 Conditional PDF:
 - $f_{Y|X} (y|x) = \frac{f_{X,Y}(x,y)}{f_X(x)} = \frac{f_{X|Y}(x|y)f_Y{y}}{f_X(x)}$
 - $X,Y$ indep if $f_{X,Y}(x,y) = f_x(x)f_y(y)$ for all $x,y$
 
 Dependent example:
 - Uniform in disc $x^2+y^2 \leq 1$, $f(x,y) = {\frac{1}{\pi} , x^2 + y^2 \leq 1 and 0 \text{otherwise}}$
 - $f_x(x) = \int_{-\sqrt{1 - x^2}}^{\sqrt{1 - x^2}} \frac{2}{\pi} \sqrt{1 - x^2}, -1 \leq x \leq 1$, and this is not uniform (only the joint is uniform)
 - To find the conditional PDF:
    - $f_{Y|X}(y|x) = \frac{1\\pi}{3\\pi \sqrt{1 - x^2}}$ if $-\sqrt{1-x^2} \leq y \leq \sqrt{1 - x^2}$
    - $Y|X \sim Unif(\sqrt{1 - x^2}, \sqrt{1 - x^2})$
        - given we know what X is (treating X as a constant), [which means $Y|X=x \sim Uniform(-\sqrt{1-x^2},\sqrt{1- x^2})$]
    - we see that in general: $f_{X,Y} \neq f_x(X)f_y(Y)$
 - NOTE: know your limits of integration!!!

 2-D LOTUS:
 - Let $(X,Y)$ have joint PDF $f(x,y)$ and let g(x,y) be a real-valued fn of x and y
 - Then $E(g(X,Y)) = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} g(x,y)f(x,y) dxdy$

 Theorem:
 - If X,Y are independent, then $E(XY) = E(X)E(Y)$
 - indep immplies uncorrelated
 - $E(XY) = \int\int x y f_x(x)f_y(y) dxdy$
    - NOTE: $\int y f_y(y) \int x f(x) dxdy $, we know $\int x f_x(x) dx = E(x)$

Ex. $X,Y \sim i.i.d Unif(0,1)$
- Find $E|X-Y|: $
    - LOTUS: $\int_{0}^{1} \int_{0}^{1} |x-y| dx dy$
    - $= \int\int_{x \gt y} (x-y)dxdy  + \int\int_{x \lt y} (y-x) dxdy = 2 \int_{0}^{1} \int_{y}^{1} (x-y) dxdy = 2 \int_{0}^{1} (\frac{x^2}{2} - yx)|_{y}^{1} dy = 1/3$
- You are picking 2 random points on a line, intuitively the average distance is probably 1/3rd
- Another way to think about problem
    - Let $M = max(X,Y)$
    - Let $L = min(X,Y)$
    - $|X - Y| = M - L$
    - $E(M - L) = \frac{1}{3}$
    - $E(M) - E(L) = \frac{1}{3}$
    - $E(M + L) = E(M) + E(L)$

- Chicken and egg problem
    - N eggs, $N \sim Pois(\lambda)$, each hatch w prob p independently
    - Let X = \# that hatch, so $X | N \sim Bin(N,p) $
    - Let Y = \# dont hatch
    - so $X + Y = N$
    - Find joint PMF of X and Y:
        - $P(X =i,Y = j) = \Sigma_{n=0}^{\infty} P(X=i,Y=j|N = n)P(N = n)$, 
            - for this infinite sum, we can simply think of $P(X=i,Y=j|N = n)$ is only $\gt 0$ if $i+j = N$
            - so that is the only term left
        - $= P(X =i,Y= j) = \Sigma_{n=0}^{\infty} P(X=i,Y=j | N = n) P(N = n) = P(X = i,Y=j |N = i+j)P(N = i+j)$
        - $= P(X = i |N = i+j)P(N = i+j) = \frac{(i+j)!}{i! j!}{i! j!} p^i q^j \frac{e^{-\lambda} \lambda^{i+j}}{(i+j)!} , p+q = 1$
        - X and Y are independent, $X \sim Pois(\lambda p), Y \sim Pois(\lambda q)$
        - NOTE: this is only true for the Poisson