# the shop is NanMenKou branch store.

## Examination

- what
    - I jumped to the conclusion.
- context
    - when
        - 2025/06/29, 10pm
        - for 1h
    - where
        - at Changsha walking street
- symptoms
    - GOAL: I wanted to buy discounted snacks at the target shop.
    - I checked meituan app, and found 2 nearby branch stores.
    - LOCATION: The target one is near NanMenKou.
    - JUMP: Then I thought that it is the NanMenKou branch store.
    - FEW: However, the NanMenKou branch store only had a few discount options in Meituan.
    - NOT_BUY: I was disappointed, and went to the KFC next door.
    - I suddenly found that the other branch store in Meituan is just meters away which provides many options.
    - TEST: I rush to it, and ask the clerk. She confirmed that it is the other branch store - walking street NO.2 branch store.
    - LATE: I delayed buying for 1h, and there was a few snacks left, so I could only choose an available but suboptimal option.

## Root cause analysis

### a few snacks left

- LATE
- 
### I give up the store --> LATE

- SYS
    - ~~I~~
    - I-STORE
        - MISMATCH
            - STATE
                - ~~DISLIKE~~: I like the store.
                - INCAPABLE
                    - ~~PSY~~: I know how to get discounts in meituan.
                    - ~~PHY~~: the process is easy.
            - BEHAVIOR
                - I_CHECK_NMK_STORE
                - ~~NOT_BUY~~(I did not choose anyone from the NMK store in meituan): right. This store does not have the discounts that I wanted.
        - ~~LOOSE~~: no external interference.
    - ~~STORE~~: The store has discounts.
- ENV
    - DEP
        - ~~ENERGY~~: The store had electricity.
        - ~~TIME~~: It was open at the time.

### I jumped --> I_CHECK_NMK_STORE

- I
    - PSY
        - RULE
            - **IGNORANCE_CRITICAL_THINKING**
                - TEST
                    - BY_MYSELF
                        - STATE
                            - AUTHENTICATION
                                - BUILDING
                                    - BIOMETRICS
                                        - OUTER_APPEARANCE
                                        - SPECIFIC_LOCATION
                    - BY_OTHERS
                        - 3RD_PARTY
                            - BAIDU_MAP(narrow candidates with a map app )
                - CAUSE
                    - RISK
                        - MANY_FACTORS
                            - LOCATION_NAME
        - STATE
            - VIEW
                - IT_NMK_BRANCH_STORE(The target is the NMK branch store)
                - NEGLECT_CRITICAL_THINKING(handle the issue of what the name of the target store is)
                    - TEST
                        - BY_OTHERS
                            - AUTHORITY
                                - OFFICIAL(ask the clerk when passing by)

            - EMOTION
                - IMPATIENT
    - PHY
        - NEURO
            - TIRED_BRAIN
- ENV
    - ~~DEP~~
    - INPUT
        - ACTIVE
            - ~~IMPEL~~: no
        - PASSIVE
            - ~~NATURE~~
            - HUMAN
                - TEMPTATION
                    - IT_NEAR_NMK(The target store is near NMK)
                    - NEGLECT_IT_IN_WS(The target is actually in the range of the walking street.)
                    - NOISE(The WS was too noisy for thinking.)

## Solutions

### a few snacks left

- LATE: other's fixed system. come the next time earlier. **<1>**

### I give up the store

- I_CHECK_NMK_STORE: mental stimulation. **<2>**

### I jumped

- AUTHENTICATION: think of and practice the method of authentication in test. **<3>**
- BAIDU_MAP: think of and practice to search a map with keywords and general location for candidates. **<4>**
- NAME_TRAP: notice that  **<5>**
    - the name of a store might or might not indicate its location.
    - there might be stores with similar names.
- IT_NMK_BRANCH_STORE: ~~reasoned view.~~  
- OFFICIAL: practice to consult the official bravely. **<7>**
- IMPATIENT: deep breathe **<8>**
- TIRED_BRAIN: have a rest. **<10>**
- IT_NEAR_NMK: ~~truth.~~
- NEGLECT_IT_IN_WS: practice to be sensitive to the specific env of a building. **<12>**
- NOISE: block it with earplugs. **<13>**

## Analysis of Solutions

### Comparison
| Solution | Cost | Effective Duration | Side Effects & Risks |
| --- | --- | --- | --- |
| 1 | HIGH | 1d | NO |
| - | - | - | - |
| 2 | LOW | 1d | FORGET |
| - | - | - | - |
| 3 | HIGH | LONG | NO |
| 4 | MIDDLE | LONG | NO |
| 5 | MIDDLE | LONG | NO |
| 7 | MIDDLE | LONG | FAKE_PROMOTION |
| 8 | LOW | HOURS | NOT_WORKING |
| 10 | MIDDLE | HOURS| NOT_WORKING |
| 12 | MIDDLE | LONG | NO |
| 13 | LOW | LONG | NO |

### Priority & Trace
[try from treatments to prevention based on time bound]: #

- [ ] 1
- [ ] 2
- [x] 13
- [ ] 4
- [ ] 5
- [x] 12
- [x] 7
- [ ] 3
- [x] 8
- [x] 10