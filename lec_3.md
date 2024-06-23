# Birthday problem
- Problem Setting: k people, find prob that 2 ppl have the same birthday
- Assumption:
    - Exclude Feb 29
    - assume other 365 days are equally likely
    - assume indep of births (one person's bday doesnt affect another person's )
- if $k \gt 365$:
    - imagine you have 365 boxes, you are putting dots (people) into these boxes
    - if you have more dots than boxes you will end up with a box that has multipple dots
    - hence prob is 1 (pigenholde principle)
- if $k < 365$:
    - $P(no match)  =  \frac{365 * 364 * 363 ... (365-k+1)}{365^k}$
        - Intuition:
            - Numerator:  
                - for the first person they can have 365 days to choose from as their bday, then the second person comes, 1 day is taken so 364, so on until the kth person you have 365-k +1 choices
            - Denominator:
                - each person has 365 days  
    - $P(match) = 1 - P(no match)$
    - Intuition:
        - you have $k \choose 2$ number of pairs, and you get a large number of pairs

- Axioms of probability 
    - $P(\phi) = 0$, $P(S) = 1$:
    - $P(\cup^\infty A_n) = \Sigma_{n=1}^{\infty} P(A_n)$ **iff** $P(A_1), P(A_2), P(A_3)...$ are disjoint, they dont overlap 

- Properties
    - $P(A^c) = 1 - P(A)$
        - Proof:
            - $1 = P(S) = P(A \cup A^c)$
    - If $A \subseteq B$,then $P(A) \leq P(B)$
        - Proof:
            - $B = A \cup (B \cap A^C)$, disjoint
            - $P(B) = P(A) + P(B \cup A^C) \geq P(A)$ 
    - $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
        - Proof (inclusion and exclusion):
            - $P(A \cup B) = P(A \cup (B \cap A^C)) = P(A) + P(B \cup A^C)$
            - Since we want that $P(A) + P(B) - P(A \cap B)$
            - We want to prove that $P(B \cup A^C) + P(A \cup B) = P(B)$
            - This is true because we know that $A \cup B$ and $A^C \cup B$ are disjoint, so the union must be $B$
    - Inclusion Exclusion prooblem: (good for finding the probability of the union)
    $$
    P(A_1 \cup A_2 \cup ... A_n) = \Sigma_{j=1}^{n} P(A_j) - \Sigma_{i<j} P(A_i \cap A_j) + \Sigma_{i<j<k} P(A_i \cap A_j \cap A_k) + ... + (-1)^{n+1} P(A_1 \cap A_2 \cap ... A_n)
    $$

    - deMonMort's problem matching problem
        - you have n cards labelled 1,2,...,n.
        - Let $A_j$ be the event that "jth card matches", or jth card in the deck matches the number on the card
        - We want to find the union: $P(A_1 \cap A_2 \cap ...\cap A_n)$ , meaning there is at least 1 match.
        - What is $P(A_j)$?
            - $P(A_j) = \frac{1}{n}$
            - all positions are equally likley, it can be anywhere of the 52 cards
        - What is $P(A_1 \cap A_2) = \frac{(n-2)!}{n!} = \frac{1}{n(n-1)}$ 
        - $P(A_1 \cap A_2 \cap ... A_k) = \frac{(n-k)!}{n!}$
        - $P(A_1 \cup A_2 \cup ... \cup A_n) = n * 1/n  - \frac{n(n-1)}{2!} * \frac{1}{n(n-1)} +  \frac{n(n-1)(n-2)}{3!} * \frac{1}{n(n-1)(n-2)} ...$ 
        - $ = 1 - \frac{1}{2!} + frac{1}{3!}  + \frac{1}{4!} + (-1)^n \frac{1}{n!}$ 
            - the last term means the case where all cards have a match
        - $P(no match) = P(\cap_{j=1}^{n}A_j) = 1/e$