# Arm Pain in Typing

## Examination
[problem overview]: #

My arms feel painful and sour.

### Context

#### When
[Specification: year, season, daytime, during & after some events]: #

-	**[DURING_TYPING]** When typing for 30 seconds.

#### Where
[Localization]: #

-	My wrists 
-	Upper arms.
-	shoulders.

### Symptoms
[avoid biases]: #
[comparison between actuation and expectation]: #
[collect evidence used by hypothesis built in the root cause analysis phrase]: #
[specification: location, degree]: #

#### Vision

-	My wrists get close to the table gradually.
-	When in a hurry or serious, I tend to get my arms off my body and hang in the air.
-	My shoulders rise up gradually.

#### Hearing

#### Smell

#### Taste

#### Touch & Feel

-	**[WRISTS_LIFT]** Lifting my wrists up relieves pain in wrists.
-	Putting shoulders down relieves pain in shoulders.
-	**[MORE_HAND_TILT]** The feeling gets more intensive when hand tilt degree increases.
-	**[ARM_OUTWARD]** the extremely sour feeling when moving arms outward further.

## Root Cause Analysis
[backward cause reasoning for general problems]: #
[recursive trouble shooting for engineering problems to an atomic level (build hypothesis, use evidence (examination  + unit tests))]: #

```mermaid
flowchart BT
	TYPING --> PAIN
```
TYPING
:	Typing causes my wrist pain.
	
	Evidence
	:	Pos
		:	-	**[DURING_TYPING]**


### Wrist Pain

```mermaid
flowchart BT
	HAND_TILT_BACK --> WRIST_PAIN
```

HAND_TILT_BACK
	:	The hand position of being tilt backward causes the sour feeling.
		
	Evidence
	:	Pos
		:	-	**[WRISTS_LIFT]**
			-	**[MORE_HAND_TILT]**
			-	(rationalism: knowledge)
				
~~OTHERS~~
:	Evidence
	:	Neg
		:	-	**[WRISTS_LIFT]**
			
### Upper Arm Pain
```mermaid
flowchart BT
	ARM_STRERCH_OUTWARD --> UPPPER_ARM_PAIN
```

ARM_STRETCH_OUT
:	The action that arms stretch outward causes the arm pain.

	Evidence
	:	Pos
		:	-	**[ARM_OUTWARD]**

### Shoulder Pain
		
## Brainstorming
[removal of touchable physical objects is applicable]: #
[replacement V.S repair. Localize the problem to an atomic level where fixing it components is more expensive than replacing it as a whole]: #
 
## Analysis of Solutions

### Comparison
| Solution | Cost | Effective Duration | Side Effects |
| --- | --- | --- | --- |
 
### Priority & Trace

## Thinking
[Lessons learned from this experience]: #
-	For senses
	-	avoid removal of neural pathways: sensor --> pathway --> brain
	-	start reasoning from the stimuli.

-	Typing is an good interaction, and arm pain is a side effect.

	**To analyse what I am doing.**

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkzODc3OTkzM119
-->