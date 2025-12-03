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
            - a system to inform the user something about an APP **when the APP is not at foreground.**
        - purpose
            - efficiency
                - keep updated
            - safety
                - avoid missing
    - body
        - components
            - APP
            - OS
        - management
            - interaction
                - interface
                    - CHANNEL_BASED: The OS decides which notification presentation types are enabled for each channel of each APP.
                - data transfer
                    ```mermaid
                    flowchart LR
                    A(APP)
                    O(OS)

                    A -->|notification request| O
                    ```
                - mode
                    - whole process
                        1. Event: An event occurs inside an APP.
                        2. App check: The APP checks if the notification is enabled for this type of event
                        3. Send: if enabled then the APP sends a notification request to the OS.
                        4. Os check: The OS checks the presentation config for this request.
                        5. Display: The finally notification is displayed.

- APP
    - channels
        - event types
- OS
    - body
        - components
            - notification presentation
            - configs
                - APPs
                    - channels
            - system mode
        - management
            - data transfer
                ```mermaid
                flowchart LR
                subgraph I
                    C(channel config)
                    M(system mode)

                    C---|intersection|M
                end
                P(final presentation)

                I -->|determine| P
                ```
- notification presentation
    - body
        - component
            - vision
                - notification drawer
                - status bar
                - banner
                - badge
                - lock screen
            - hearing
                - sound
                - vibration
        - management
            - interaction
                - modes                
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
- system mode
    - normal
    - DND
    - silent
    
    | Aspect | DND | silent |
    | --- | --- | --- |
    | Purpose | not to disturb the device user itself | not to disturb others |
    | config labor | high | low |
    | config grain level | APP | system |
    | enable different profiles | Y | N |
    | enabled presentation component | notification drawer | vision |
    | use cases | 1. work 2. sleep | in public space |
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
        - management
            - interaction
                - exception
                    - certain APPs
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
