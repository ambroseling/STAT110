# Conditional Probability
- Indepdence
    - events A and B are independent if $P(A \cap B) = P(A)P(B)$
    - independence tells us if A occured, we have no info on whether B occurs
    **NOTE**: completely different from disjointness !!!
        - disjointed is if A occurs, B cant occur (A disjoint from B, A and B are disjoint)
        - $A,B,C$ are indep if :
            - $P(A,B) = P(A)P(B)$
            - $P(A,C) = P(A)P(C)$
            - $P(B,C) = P(B)P(C)$
            - $P(A,B,C) = P(A)P(B)P(C)$
        - Similarly for events $A_1,...A_n$
- Newtown Pepys Problem,
    - **NOTE**: when you see 'at least', you think of 'union',if you do the compliment it will be the 'intersection'
    - have fair 6 sided dice, which is most likely?
    - 1. A - at least one 6
    - 2. B - at least two 6s with 12 dices
    - 3. C - at least three 6s with 18 dices
    - $P(A) = 1 - (5/6)^6$
    - $P(B) = 1 - (5/6)^12 - 12(1/6)(5/6)^11$
        - $(5/6)^12$: probability that there are no 6s
        - $12(1/6)(5/6)^11$: probability that there is exactly 1 6
    - $P(C)  = 1 - \Sigma_{k=0}^{2} {18 \choose k} (1/6)^{k} {5/6}^{18-k}$


- Conditional probability
    - how should you update your probability / beliefs / uncertainty based on new evidence
    - Conditioning is the soul of statistics
    - Def:
        - $P(A|B) = \frac{P(A \cap B)}{P(B)}$ , if $P(B) > 0$
        - Intuition 1:
            - you have some sample space $S$
            - 9 pebbles (possible outcomes), total mass = 1
            - Some event is a set of pebbles 
            - $P(A|B)$: we know that B occurs so get rid of the pebbles outside of B  (or $B^C$), lets say you have some other event A, you make another circle, you find where they intersect
            - then you renormalize to make the total mass 1 again
    - Theorem 1:
        - $P(A \cap B)  = P(B) P(A|B) = P(A)P(B|A)$
    - Theorem 2:
        - $P(A_1,...,A_n) = P(A_1)P(A_2|A_1)P(A_3|A1,A_2)...P(A_n|A_1,...,A_n-1)$ 
    - Theorem 3:
        - $P(A|B) = \frac{P(B|A)P(A)}{P(B)}$