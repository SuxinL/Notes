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


- arms.


### Symptoms
[avoid biases]: #
[comparison between actuation and expectation]: #
[collect evidence used by hypothesis built in the root cause analysis phrase]: #
[specification: location, degree]: #

#### Vision

-	I bend my arms when typing.
-	**[ARMS_HUNG]** I tend to get my arms off my body and hung in the air.

#### Hearing

#### Smell

#### Taste

#### Touch & Feel

-	**[ARM_OUTWARD]** the extremely sour feeling when moving arms sideways further.

## Root Cause Analysis
[backward cause reasoning for general problems]: #
[recursive trouble shooting for engineering problems to an atomic level (build hypothesis, use evidence (examination  + unit tests))]: #

```mermaid
flowchart BT
	TYPING --> ARM_PAIN
```

TYPING
:	I_BEND_ARMS
	:	The action that I bend arms causes the feeling.
		
		Evidence
		:	Pos
			:	-	Bending down for a while causes a sour feeling.
				-	Bending legs when sleeping causes uncomfortable feeling.
				-	When the pain appears, stretching arms forward relieves it instantly.
				-	**[ARMS_HUNG]** This change decreases the level of bending.
		
		>	Notice:	To main a typing position for a long time, I need to bend arms.
		>
		>	If I switch to stretch my upper arm and forearm to a straight line, 
		>	-	without external supports, it is painful.
		>	-	with external supports, hand movements are hindered.
			 
		BEND_SIDEWAYS
		:	Evidence
			:	Pos
				:	-	**[ARM_SIDEWAYS]**
						
		BEND_BACKWARDS
		
```mermaid
flowchart BT
	BEND_SIDEWAYS
	SIDEWAYS_THOUGHT --> BEND_SIDEWAYS
	SIDEWAYS_ENV --> BEND_SIDEWAYS
```		

SIDEWAYS_THOUGHT
:	Unconsciousness.

SIDEWAYS_ENV
:	FAR_KEYBOARD
	:	When the keyboard is far away, my arms stretch sideways. 	 

	SHOULDERS_RAISED
	:	When shoulders are raising, my arms stretch sideways.

```mermaid
flowchart BT
	I_RAISE_SHOULDERS --> SHOULDERS_RAISED
	RAISE_THOUGHT --> I_RAISE_SHOULDERS
	RAISE_ENV --> I_RAISE_SHOULDERS
```	

RAISE_THOUGHT
:	unconsciousness

RAISE_ENV
:	HUNCHBACK

	HURRY
	
## Brainstorming
[removal of touchable physical objects is applicable]: #
[replacement V.S repair. Localize the problem to an atomic level where fixing it components is more expensive than replacing it as a whole]: #

SIDEWAYS_THOUGHT
:	remember and practice to hang arms near the body. **<1>**

FAR_KEYBOARD
:	move it to near the body. **<2>**

SHOULDERS_RAISED
:	lower shoulders when noticing them.

## Analysis of Solutions

### Comparison

| Solution | Cost | Effective Duration | Side Effects |
| --- | --- | --- | --- |
| 1 | MIDDLE | LONG | LITTLE |
| 2 | LOW | LONG | **<HOLDING_ARMS>**|
| 3 | LOW | LONG | HINDER:	It hinders the movement of hands. |

**<HOLDING_ARMS>**
:	This method enables the whole arm and hand in a straight line, which however needs supports.
	-	If letting muscles to support the posture, it takes energy and brings pain.
	-	external supports: hindering movements.
		- supporting wrists	
		- supporting arms:	additional equipment with considerable heights needed.
		 
### Priority & Trace

-	*1*
-	*2*

	It makes arms relaxed to put them on soft tissue paper packages. But they hinder hands' movement.
	
-	3

## Thinking
[Lessons learned from this experience]: #
-	When reasoning in an unfamiliar field, the whole process is just repeating a step, we can find clues from
	-	systematic learning 
	-	examine the posture, and think about which actions cause similar results.
-	**How to handle the trade-off between different approaches?**
-	refinement of solutions: When a solution solves a problem, it might brings new problems.
-	When an action has side effects, specify the motions to find which one cause the side effects.
	-	intensity
	-	direction	
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExODYwMjM4MDksLTQzMzczNjMyXX0=
-->