Covariance:
- variance of a sum
- we ahve $X$ and $Y$
- Defn: $Cov(X,Y) = E((X-EX)(Y-EY)) = E(XY) - $
- since $E(XY) - E(X)E(Y) + E(X)E(Y) + E(X)E(Y)$
- Properties:
    - Cov(X,X) = Var(X)
    - Cov(X,Y) = Cov(Y,X)
    - Cov(X,c)= 0 if c is constant
    - Cov(cX,Y) = c Cov(X,Y)
    - Cov(X,Y) = Cov(X,Y) + Cov(X,Z)
- Practice: $Cov(X+Y,Z+W) = Cov(X,Z) + Cov(X,W) + Cov(Y,Z) +Cov(Y,W)$
- $Cov(\Sigma_{i=1}^{m} a_i X_i, \Sigma_{j=1}^{n}b_jY_j) = \Sigma_{i,j} a_i b_j Cov(X_i,Y_j)$
- $Var(X_1+X_2) = Var(X_1) + Var(X_2) + 2 Cov(X_1,X_2)$
- NOTE: if $X_1$ and $X_2$ are independent, the $2Cov(X_1,X_2)$

- $Var(X_1 + ... + X_n) = Var(X_1) + Var(X_2) + ... + Var(X_n) + 2 \Sigma_{i \lt j} Cov(X_i,X_j)$
- Theorem: If X,Y are independent they are uncorrelated, i.e. $Cov(X,Y) = 0$, Converse is false
- so if $Cov(X,Y) = 0$, they may not be independent
    - Example:
        - $Z \sim \mathcal{N}(0,1), X = Z, Y = Z^2$
        - $Cov(X,Y) = E(XY) - E(X)E(Y) = E(Z^3) - E(Z)E(Z^2) = 0$
        - But they are clearly not independent, Y is a function of Z, if you know X you immediately know Y and Y detemines magnitude of X

- Definition Correlation: 
    - $Corr(X,Y) = \frac{Cov(X,Y)}{SD(X)SD(Y)} = Cov(\frac{X-E(X)}{SD(X)},\frac{Y-E(Y)}{SD(Y)})$
    - Correlation is a dimensionless quantity
    - SD is a sq of variance
    - its called standardization $X - EX$ and $Y - EY$ so it has zero mean 
- Theorem: Correlation is always btw -1 and 1
    - $-1 \le Cov(X,Y) \le 1$
    - Proof:
        - WLOG, assume X and Y are standardized
        - let $Cov(X,Y) = \rho$
        - $0 \lt Var(X+Y) = Var(X) + Var(Y) + 2 Cov(X,Y) = 2 +  2 \rho$
        - $ 0 \lt Var(X-Y) = Var(X) + Var(Y) - 2Cov(X,Y) = 2 - 2 \rho$
        - these 2 inequalities say correlation must be btw -1 and 1



- $Cov$ in a multinomial
    - $(X_1,...X_k) \sim Mult(n,\vec{p})$
    - Find Cov(X_i,X_j) for all i,j
        - If $i = j, Cov(X_i,X_i) = Var(X_i) = n p_i (1-p_i)$
            - use variance of binomial
        - Cov(X_1,X_2) 
            - you expect it to be negatively correlated
            - putting people in categories, if you put more people in X_1 you expect less people in X_2, less ppl left over
        - $Cov(X_1,X_2) = c \cdot Var(X_1,X_2) = n p_1 (1-p_1) + n p_2 (1-p_2) + 2 \cdot c$
        - We can also think of Var(X_1 + X_2) as lumping together 2 categories into 1 big category (success = in category 1 or category 2)
        - $Var(X_1 + X_2) = n(p_1 + p_2)(1 - (p_1 + p_2)) = Cov(X_1,X_2) = - n p_1 p_2$
    - General:
        - $Cov(X_i,X_j) = -n p_i p_j$ for $i != j$

- Variance of binomial
    - $X \sim Bin(n,p)$ write as X = X_1 + ... + X_n
    - $X_j$ i.i.d $Bern(p)$
    - $VarX_j = EX_j^2 - EX_j^2$
