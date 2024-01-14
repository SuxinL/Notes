# Multiple Factor Authentication

Multiple Factor Authentication is a kind of authentication process in which more than one **type** of authentication methods are used to improve login security.

## Types
- knowledge factors
	- passwords
	- pins
	- keystrokes
	- security questions
- inherent factors
	- fingerprints
	- voices
	- facial features
- possession factors
	- hardware
		- physical keys
		- credit cards
	- software
		- static
			- public-key authentication
		- dynamic
			- OTP
				- network needed
					- SMS
					- calls
					- emails
				- network not needed
					```mermaid
					flowchart
						S(seed)
						K(key)
						A(algorithm)
						T(token)

						S --> A
						K --> A
						A --> T
					```
					There are 2 types of OTPs based on types of seeds
					- click: HOTP
					- time: TOTP
	
					| Aspect | HOTP | TOTP |
					| --- | --- | --- |
					| Advantages | Harder to break by brute-force attacks | 1. fewer human interactions 2. having a lifespan and less time for theft |
					| Shortcomings | 1. Hackers can use it anytime before the user.  2. Unsync due to excessive presses on the counter | time drift |
						
					TOTP can be implemented as hardware or software	
					- hardware: key fobs
					- software: authenticator apps
					
					| Aspect | HW | SW |
					| --- | --- | --- |
					| Advantages | totally offline | no special equipment needed, time is accurate |
					| Shortcomings | 1. easy to lose or misplace 2. time drift after a period | potential malware in the same device |			 
- behavioral factors
	- location
	- devices
	- ip

| Type | Advantages | Shortcomings |
| --- | --- | --- |
| Knowledge | simple, flexible | vulnerable to phishing, snuffing, brutal force and social engineering attacks |
| Inherent | stable, can not forget, the safest one | high cost equipment, hard to change once compromised |
| Possession | stable | vulnerable to phishing, snuffing, stealing and MIIM attacks |
| Behavior | no operations needed from user side | large resources needed |

	
		
		 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA1NzI4ODYxM119
-->