# Android Notification System

- env
    - in
        - dep
            - energy
                - electricity
            - service
                - device
        - input
            - instruction
                - user inputs
            - raw material
    - out
        - target
            - output
                - notification presentation
            - object
                - user
        - waste
- sys
    - main points
        - what
            - a system to inform the user something about an APP from outside the APP.
        - purpose
            - efficiency
                - keep updated
            - safety
                - avoid missing
    - body
        - components
            - APP
            - OS
            - notification presentation
        - management
            - interaction
                - interface
                    - CHANNEL_BASED: The OS decides which notification presentation types are enabled for each channel of each APP.
                - data transfer
                    ```mermaid
                    flowchart LR
                    A(APP)
                    O(OS)

                    A -->|notification request| O --> N[/notification presentation/]
                    ```
                - mode
                    - whole process
                        1. EVENT_OCCUR: An event occurs inside an APP.
                        2. APP_CHECK: If notification is enabled for this type of event, then the APP send a notification request to the OS.
                        1. CHANNEL_CHECK: The OS decides which presentations are enabled for this request.
                        2. MODE_CHECK: The OS checks the current system mode for additional filters.
                        3. DISPLAY: The finally allowed presentations are displayed.
- notification presentation
    - body
        - types
            - vision
                - notification drawer
                - status bar
                - banner
                - badge
                - lock screen
            - hearing
                - sound
                - vibration
- APP
    - channels
        - event types
- OS
    - body
        - components
            - APPs config
                - channels config
        - management
            - OS modes
                - normal
                - DND
                - silent
                
                | Aspect | DND | silent |
                | --- | --- | --- |
                | Purpose | not to disturb the device user itself | not to disturb others |
                | config labor | high | low |
                | config grain level | APP | system |
                | enable different profiles | Y | N |
                | use cases | 1. work 2. sleep | in public space |
            - channel config modes
                - off
                - silent
                - snooze
                - normal
                - private
                - important

                | mode | target channels | enabled presentation types|
                | --- | --- | --- |
                | off | 1. no value 2. distractions | no |
                | silent | 1. not important 2. while using the device like notifications from VPNs or games | vision |
                | snooze | when there are more important things | the notification displays later. |
                | normal | normal | vision + hearing |
                | private | 1. message 2. finance | not display the notification details on the lock screen |
                | important | 1. message ||
- DND
    - main points
        - what
            - do not disturb self
        - purpose
            - efficiency
                - avoid distraction
                    - work
                    - study
                    - meeting
                    - sleep
    - body
        - components
            - **affected** APPs
        - management
            - interaction
                - exception
                    - starred contacts
                    - repeated calls
        - types
            - regular
            - one-time

            | Aspect | regular | one-time |
            | --- | --- | --- |
            | config labor | low: one-time investment | high: each time I need to use it I need to config |
            | risk || MISS_OUT: miss important notifications if I forget to set the duration or turn it off manually. |
            | use cases | regular events: 1. work 2. class 3. sleep | temporary events: 1. meeting 2. trip |
- regular DND
    - mind
        - what
            - DND turning on regularly
        - state
            ```mermaid
            flowchart
            ON(REGULAR ON)
            OFF

            OFF -->|a profile starts| ON
            ON -->|all started profiles end| OFF
            ON -->|turn off manually| OFF
            ```
    - body
        - components
            - profiles
- one-time DND
    - mind
        - what
            - DND for temp cases
        - state
            ```mermaid
            flowchart
            ON(ONE-TIME ON)
            OFF

            OFF -->|turn on manually| ON
            ON -->|turn off manually| OFF
            ON -->|the duration ends| OFF
            ```
- silent mode
    - The hearing presentations are muted for almost all APPs.
