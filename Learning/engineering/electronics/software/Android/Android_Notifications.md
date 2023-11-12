# Android Notification
			
- what
	- a notification is a short message
- goals
	- to notify users something about apps or the system.
- when
	- when something happens, apps generate and send notifications to android OS, which then displays them.
- how
	- system structure
		```mermaid
		flowchart
			APP -->|notifications| OS
		```
	- presentation
		- hearing
			- sound
			- vibration
		- vision
			- lock screen
			- banner
			- badge
			- status bar
			- notification drawer	
	- configuration
		- app & channel: for long term 
			- turn off: for needless ones like spams
			- silent: 
				- for less important ones needing no real-time response from other works like news
				- for ones happening only when using the phone like status changes of vpn or games
			- snooze: if there is something more important currently.
			- normal with presentations and sounds
			- hide content at the lock screen: for privacy like messages and orders
			- priority conversations: for very important contacts. 
		- system: for short term
			- silent mode: for phone using in public
			- Do Not Disturb: to avoid phone distraction in study, work or sleep
				- scope: applied to which apps, except for very important ones
					- apps like messaging
					- stared contacts
					- emergency calls
				- duration
					- one-time
					- schedule

					```mermaid
					flowchart
							START
							REGULAR
							ONE_TIME
							CLOSED
							START --> CLOSED
							CLOSED -->|a period starts| REGULAR
							CLOSED -->|turn on DND| ONE_TIME
							REGULAR -->|turn off DND| CLOSED
							REGULAR -->|a period ends| CLOSED
							ONE_TIME -->|turn off DND| CLOSED
							ONE_TIME -->|the time duration ends| CLOSED
					``` 
				- types: disabling which types of presentations. In most cases notifications are only allowed to display in the notification drawer. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI5MjU1NzczN119
-->