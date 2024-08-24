# Monty Hall problem
- Given 3 doors, 1 door has car, 2 doors have goats. Monty knows where the car is. Monty always opens a goat door. if he has a choice, he picks with equally likely. He picks with equal probability. Should you switch?

- Suppose Monty opens Door 2, we know Door 2 has a goat AND Monty opens door 2.
    - LOTP: wish we knew where car is
        - S: success (assuming switch)
        - $D_j$: door j has car (j $\in$ {1,2,3})
        - $P(S) = P(S|D_1) 1/3 + P(S|D_2) 1/3 + P(S|D_3) 1/3$
        - $ = 0 + 1/3 + 1/3 = 2/3$
    - 
    - 

# Simpsons paradox
- Dr Hibert
    -           heart   bandaid removal
    - Success:   70         10
    - Failure:   20          0
- Dr Nick
    -           heart   bandaid removal
    - Success:   2           81
    - Failure:   8            9
- You can say Nick has higher success rate but that is unconditional
- Conditional on heart and bandaid, Hibert is actually better
- A: surgery is successful
- B: treated by Dr Nick
- C: have heart surgery (confounder,control)
- $P(A|B,C) < P(A|B^C,C)$
- $P(A|B,C^C) < P(A|B^C,C^C)$
- $P(A|B) > P(A|B^C)$ 
- $P(A|B) = P(A|B,C)P(C|B) + P(A|B,C^C)P(C^C|B)$