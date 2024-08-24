# Statistics cheatsheet

Naive Probability 
- $P(A) = \text{number of favourable outcomes} / \text{number of possible outcomes}$

Axioms of probability
- $P(\phi) = 0$
- $P(S) = 1$:
    - $P(\cup^\infty A_n) = \Sigma_{n=1}^{\infty} P(A_n)$ **iff** $P(A_1), P(A_2), P(A_3)...$ are disjoint, they dont overlap 

Properties of probability:
- $P(A^c) = 1 - P(A)$
- If $A \subseteq B$,then $P(A) \leq P(B)$
- (Inclusion & Exclusion to 2 events): $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
- (Inclusion & Exclusion to N events):$P(A_1 \cup A_2 \cup ... A_n) = \Sigma_{j=1}^{n} P(A_j) - \Sigma_{i<j} P(A_i \cap A_j) + \Sigma_{i<j<k} P(A_i \cap A_j \cap A_k) + ... + (-1)^{n+1} P(A_1 \cap A_2 \cap ... A_n)
$

Law of total probabiltiy:
- $P(A) = \Sigma_n P(A \cap B_n)$

Independence:
- Events A and B are independent if $P(A \cap B) = P(A)P(B)$
- $A,B,C$ are indep if :
    - $P(A,B) = P(A)P(B)$
    - $P(A,C) = P(A)P(C)$
    - $P(B,C) = P(B)P(C)$
    - $P(A,B,C) = P(A)P(B)P(C)$

Conditional Probability:
- $P(A|B) = \frac{P(A \cap B)}{P(B)}$ , if $P(B) > 0$
- Theorem 1:
    - $P(A \cap B)  = P(B) P(A|B) = P(A)P(B|A)$
- Theorem 2:
    - $P(A_1,...,A_n) = P(A_1)P(A_2|A_1)P(A_3|A1,A_2)...P(A_n|A_1,...,A_n-1)$ 
- Theorem 3 (Bayes):
    - $P(A|B) = \frac{P(B|A)P(A)}{P(B)}$