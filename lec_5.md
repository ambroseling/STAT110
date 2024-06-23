# Conditioning / Conditional probability
- 1. try simple and extreme cases
- 2. break the problem into simple pieces
- $P(B)  = P(B \cap A_1) + ... + P(B \cap A_n)$ 
- $P(B)  = P(B|A_1)P(A_1) + P(B|A_2)P(A_2) + ... + P(B|A_n)P(A_n)$

- Ex. get random 2 card hard from standard deck
    - Find $P(\text{both aces},\text{have ace})$
        -  $\frac{P(\text{both aces},\text{have ace})}{P(\text{have ace})}$
        - $ $ 
- Tested for disease afflicts $1%$ of the population
    - Suppose tests as advertised as "95% accurate" if the patient has the disease
    - Event D: patient has disease
    - Event T: patient tests positive
    - $P(T|D) = 0.95 = P(T^C|D^C)$
    - $P(D|T) = \frac{P(T|D)P(D)}{P(T)} = \frac{P(T|D)P(D)}{P(T|D)P(D) + P(T|D^C)P(D^C)}$

- Biohazards:
    - confusion $P(B|A)$ with $P(A|B)$ (prosecutors fallacy)
    - confusion P(A) 
        - prior means before we have evidence  $P(A)$, $P(A) != P(A|A)$ 
        - posterior means after we have evidence $P(A|B)$ 

- Definition: Event A,B are conditionaly independent given C if $P(A \cup B |C) = P(A|C) P(B|C)$
    - Does conditional indep given C imply independence? NO
        - chess opponent of unknown strength
        - it may be that game outcomes are **conditionally indepedent** but not independent
        - given strength of opponents, but not independent
    - Does indepedence impy conditional independence? NO
        - A: Firealarm going off
        - casued by:
            - F: fire
            - C: popcorn
        - Suppose that F and C are independent, but $P(F|A,C^C) = 1$ but are not conditionally independent given A
