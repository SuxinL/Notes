# Meal Decision

## CASE

- PICK_LEMON_TEA: I picked a cup of lemon tea 100m away with 1.5 yuan when I was at a mall.
- WAIT_FIRED_NOODLES: I ordered fried noodles when my sleep was interrupted and I felt hungry in the morning.

## THOUGHT

### Procedure

- O: if I am outside
    - P_F: if I with others OR I really want to enjoy the flavor
        - dine-in.
    - else
        - self-pick
- I: else
    - T_B: if I feel tired OR I am busy
        - home delivery
    - N_C_N: else if no material OR self pick is very cheap AND near
        - self-pick
    - else 
        - cook