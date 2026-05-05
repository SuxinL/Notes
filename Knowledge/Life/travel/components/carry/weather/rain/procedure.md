# Rain

## CASE

- SUDDEN_RAIN_WHEN_RIDE: I encountered a sudden rain when riding, which soaked my clothes.
- HEAVY_RAIN_WHEN_WALK: It is not enough to use umbrella. The rain soaked my clothes and shoes when I walked to a temple. I need a raincoat and rain boots.
- WALK_IN_LIGHT_RAIN: In a light rain, I walked to a power station with umbrella and sneakers.

## THOUGHT

### Conditions

- rainy

### Purposes

- safety
    - clothes
    - shoes

### Principles

#### Root Cause Analysis

##### rain soaks wearing

- SYS
    - RAIN
    - RAIN-WEARING
        - MISMATCH
            - STATE
                - PROTOCOL: Water tends to be absorbed by normal clothing.
            - BEHAVIOR
                - SOAK: a physical process.
        - ACCESS
    - WEARING 
- ENV
    - DEP
        - ~~ENERGY~~
            - Test
                - State
                    - Link
                        - Neg
                            - no extra energy needed.
        - SERVICES
            - TIME
                - Test
                    - Behavior
                        - NegTest
                            - PosResult
                                - Short time exposure does not soak my clothes.
    - INPUT
        - ~~ACTIVE~~
            - Test
                - State
                    - Link
                        - Neg
                            - this is a spontaneously physical process.
        - PASSIVE
            - ~~NATURE~~
            - ~~HUMAN~~

##### I go outside in rain -> ACCESS

- SYS
    - PSY
        - RULE
            - NO_CHECK_WEATHER_HABIT
        - STATE
            - VIEW
                - IGNORANCE_RAIN_COMING
            - EMOTION
                - CRAVING_TRIP: sometime I really want to go outside to relax.
            - ~~MENTAL_DISORDER~~
    - ~~PHY~~
- ENV
    - ~~DEP~~
    - INPUT
        - ~~ACTIVE~~
        - PASSIVE
            - NATURE
                - GOOD_WEATHER_NOW: the current weather is good.
            - ~~HUMAN~~

#### Solutions

##### rain soaks wearing

- RAIN: ~~weather, out of control~~
- PROTOCOL: ~~hard to change the nature~~
- SOAK: wipe water droplets falling on clothing in time.
- ACCESS
    - CLOTHES: raincoat / umbrella
    - SHOES: rain boots / shoe covers
- WEARING: ~~MGTL~~
- TIME: try not to stay in rain for long.

##### I go outside in rain -> ACCESS

- NOT_CHECK_WEATHER_HABIT: practice to check weather forecast before going outside
- IGNORANCE_RAIN_COMING: ~~a reasoned view~~
- CRAVING_TRIP: practice self control
- GOOD_WEATHER_NOW: ~~a natural effect, out of control~~

### Procedure

1. C: clothes
    1. H_R: If heavy rain or riding
        1. C: raincoat
    2. ND: not just drizzle
        1. U: umbrella
2. S: shoes
    1. W_H_M_L: if walking in heavy rain or on a muddy road for a long time of minutes,
        - B: rain boots
        - C: plastic shoe covers if not bringing boots