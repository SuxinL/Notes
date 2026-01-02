# cold hands

## Examination

### what

- My hands feel very cold.

### context

- when
    - in winter
    - after getup, before eating
    - for months.
- where
    - at LanKaWei

### symptoms

- vision
    - My hands turned pale.
- hearing
- smell
- taste
- feeling
    - My hands are extremely cold sometimes.

## root cause analysis

### hand cold

- HAND_COLD

### hand heat lost more than generated. -> HAND_COLD

- HAND
- ENV
    - DEP
        - ENERGY
            - LESS_ENERGY
        - ~~SERVICE~~
    - INPUT
        - ACTIVE
            - CONTROL
                - HORMONE
                    - *LESS_THYROID*
        - PASSIVE
            - NATURE
                - L
                - S
                - T
                    - COLD_ENV
                        - Test
                            - Hard
                                - Neg
                                    - P
                                        - **[ONLY_WINTER]** My hands become cold only in cold winter.
            - ~~HUMAN~~

### less energy is sent to hands -> LESS_ENERGY

- CIRCULATORY_SYS
    - Effect
        - P
            - **[PALE_HAND]**
    - WEAK_HEART: weak
        - Effect
            - P
                - **[IRREGULAR_HEARTBEAT]** My heartbeats are irregular.
    - NARROW_VESSEL: narrowed
    - POOR_RED_BLOOD_CELL
        - Effect
            - P
                - **[WEAKNESS]**
                - **[PALE_SKINS]**
        - FEW
        - BAD
- ENV
    - DEP
        - ~~ENERGY~~: itself
        - ~~SERVICE~~
    - ~~INPUT~~
        - ACTIVE
            - HORMONE
        - PASSIVE
            - NATURE
            - HUMAN

### vessels become narrow -> NARROW_VESSEL

- VESSEL
    - *HIGH_BLOOD_PRESSURE*
    - PAD
- ENV
    - ~~DEP~~
    - INPUT
        - ~~NATURE~~
        - HUMAN
            - MUSCLE_CONSTRICT

### blood loses -> FEW
- I
    - DIGESTION_SYS
        - HEMORRHOIDS
            - Test
                - State
                    - Evidence
                        - P
                            - **[HEMORRHOIDS]** I have this condition and it bleeds when pooping.
- ~~ENV~~

### produce unhealthy red blood cell -> BAD

- SYS
- ENV
    - DEP
        - ENERGY
        - SERVICE
            - NUTRIENTS
                - *IRON*
                - *VB-12*
    - ~~INPUT~~
        - ACTIVE
        - PASSIVE

### brain reacts -> MUSCLE_CONSTRICT

- BRAIN
- ENV
    - ~~DEP~~
    - INPUT
        - ACTIVE
        - PASSIVE
            - NATURE
                - L
                - S
                - T
                    - COLD_ENV
            - HUMAN
                - *OVERSENSITIVE*
                - *WRONG_SENSATION*

## solution

### hand cold

- [x] HAND_COLD: ~~transient effect, a physiological feeling.~~

### hand heat lost more than generated.

- [ ] COLD_ENV: natural rule. cut the flow
    - [ ] HAND-ROOM:
        - [ ] gloves
        - [x] hot water bag
    - [ ] ROOM: 
        - [ ] hot fan
        - [ ] ac
    - [x] ROOM-OUTSIDE: close windows and doors
    - [x] OUTSIDE: ~~other's fixed system.~~

### less energy is sent to hands

- [ ] WEAK_HEART
    - [ ] medicine.
    - [x] exercise.
- [x] NARROW_VESSEL: hot drinks.
- [ ] FEW: transfuse

### vessels become narrow

- [ ] PAD: 
    - [ ] medicine
    - [x] diet
- [x] MUSCLE_CONSTRICT: ~~transient effect.~~

### blood loses

- [ ] HEMORRHOIDS:
    - [ ] surgery
    - [ ] medicine