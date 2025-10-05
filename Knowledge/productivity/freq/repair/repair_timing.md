# Repair Delay

## CASE

- CLOTHES
    - ARRIVE_HOME: I take my clothes off **each time**, otherwise
        - I feel very hot in the room soon. 
    - WASH: I wash clothes **weekly**.
        - c: the washing machine costs electricity and water.
        - h: dried clothes grow molds slowly. 
- FOODS
    - COOK
        - KITCHEN_UTENSIL: I CLEAN them **each time** after cooking.
            - e: I have only one of each tool, and I need them next time of cooking. 
            - s: easy to knock messy tools, which is dangerous especially for knives.
        - DESK: CLEAN it **weekly**
            - c: 7->1
            - h: the accumulation of wastewater and oil is slow, and they get smelly slowly.
    - EAT
        - BOWL: WASH bowls **weekly**.
            - c: moderate->mild
            - h: 
                - initial clean: as long as I rinse a bowl, it get moldy slowly.
- LIVING
    - KEY_PHONE: I restore keys and my phone **each time** when I come back, otherwise 
        - e: hard to find them
        - s: it costs a large amount of money if I forget to switch my phone into Wifi mode before using the network. 
    - TOILET: I FLUSH the toilet **each time**.
        - e: I have only one.
        - s: accumulated wastes are really smelly.
    - SLEEP: I CLEAN the bed and nightstand **each time** when I get up.
        - e: structure
    - DESICCANT_BAG: I refill it **weekly**. 
        - full & empty
    - WASTE_BIN: I CLEAN it **weekly**
        - c: 7->1
        - h: **food remains smell and attract cockroaches**
            - initial clean: throw food remains out each time
- TRAVEL
    - MOTORCYCLE: I charge it **weekly**
        - full & empty
- WORK
    - PHONE
        - BACKUP: backup photos **daily**
            - c: moderate->mild
            - h: at most photos taken today are lost.
        - UPDATE: update apps **monthly**
            - c: ~4->1
            - h: a small update will not improve my use much.
        - CLEAN: clean storage **monthly**
            - c: moderate->mild
            - h: Data accumulates slowly, and I can notice that my phone slags only if there is only little space.
            - s: avoid deleting important data before careful thinking.
    - LAPTOP
        - UPDATE: update apps **monthly**
            - c: ~4->1
            - h: small updates do not change much.

## THOUGHT

### CONDITION

- CLEAN
- BACKUP
- UPDATE

### PURPOSE

- efficiency
    - cost
        - LOW_OVERALL: a low overall cost of repair
    - object
        - STATE: maintain a good state of the target
    - env
        - STRUCTURE: maintain a good structure of whole system
- safety
    - object
        - ERODE
        - KNOCK
        - LOST
    - env
        - ODOR
        - PEST

### PRINCIPLE

- GENERALIZATION: the repair can be
    - clean: protect a tool from wearing, erosion and missing
    - backup: protect data from missing
    - update: save a user from attacks due to bugs and from poor efficiency due to outdated tools.
- BALANCE
    - find a repair **freq** to reach a good balance between the overall repair cost and harm of delay
- COST_REDUCTION
    - FREQ: for a single target, reduce the freq of repair.
    - BATCH: for a group of copies, handle them together.
- STRUCTURE_ALWAYS: even if I decide to delay the repair, put the object at a good location.
    - bowls in the pool
    - clothes in the washing machine
- **SCHEME**
    1. REPAIR_COST
        - CHEAP: if cheap then repair now easily
            - rinse
            - transfer a physical object
        - COSTING: requires a complex tool
            - wash with cleaner
            - transfer via the wild Internet
    2. IDLE_ACCUMULATION: the harm accumulation **when the object is idle after being used**.
        - FAST: if fast then I have to repair immediately after using.
            - DANGEROUS: clean dangerous tools
                - sharp
                - slippery
                - sticky
                - smelly
            - CRITICAL: clean critical things
                - property
                    - keys
                    - money
                    - ids
                    - credentials
                    - electronics
                - privacy
                    - data
                    - password
            - SPOIL: things that spoil fast.
                - food
                - powder
                - medicine
        - **PRE_REPAIR**: For some cases I can do a simple repair to slow the harm of spoil largely.
            - rinse a bowel 
            - squeeze a piece of clothes
        - SLOW: if slow then I can repair later.
    3. COPIES: if I can get multiple copies of the object easily, then repair them as a batch in the end.
        - clean
            - bowls
            - clothes
        - backup 
            - photos
    4. USE_ACCUMULATION: else if the harm accumulation is also slow during using, I can repair it after multiple times of use (reduce freq). 
        - clean
            - the cooking desk
            - the floor
            - the waste bin
            - comforter
            - not dirty clothes
            - shoes
            - storage
        - backup
            - a project
        - update
            - an app
        - maintain
            - vehicles
            - electronic devices
    - FREE_TIME: In the end if I have only a single one which must be repair before reusing but I do not hurry, then take my time.

### PROCEDURE

1. LC_HI: if low repair cost OR high idle harm accumulation
    - N: repair now. 
2. M: I can get multiple copies,
    - B: repair as a batch in the end.
3. LU: if low use harm accumulation
    - R: repair after multi-reuse
4. F: repair when free before reusing
