# ThinkPad Interfaces

## Structure
- Basic UI
    - get(output)
        - display screen
        - speakers
        - signal lights
            - [power button](#power-button-light-and-lid-light)
            - [lid](#power-button-light-and-lid-light)
            - AC connector
            - speaker muted
            - mic muted
            - Fn lock
            - Caps lock
            - camera
    - set(input)
        - power button
        - keyboard
        - [TrackPoint](TrackPoint.md)
        - [touch pad](#touch-pad)
        - touch screen
        - camera
        - mic
- Extensions
    - multimedia connectors
        - audio
            - headphone-mic
        - video
            - HDMI
            - DP
    - USB connectors
        - USB 3.0
        - [always-on USB 3.0](#always-on-usb)
    - storage slots
        - SD
    - networks
        - ethernet connector
        - SIM slot
    - workstation connectors
        - docking
- Security
    - fingerprint sensor
    - security lock
    - smart card reader
    - emergency-reset hole
- Power
    - AC adapter connector

## Power Button Light and Lid Light

The power button light and lid light behave the same way and represent the system status.

| Light Status | System Status |
| --- | --- |
| On | Running |
| Off | Turned off or in hibernation |
| Blinking fast | Entering into suspend mode |
| Blinking slowly | In suspend mode |
| Blinking 3 times | Starting to charge |

## Always-On USB

Normal USB connectors and always-on USB connectors behave differently in conditions of charging external devices.

Normal USB connectors can be used to charge devices only when the system is running.

Always-on USB connectors are available for charging in any of the following 3 conditions:
- the system is running
- the system is suspended
- the system is turned off or in hibernation, and the laptop is charging.

## AC Connector Status Light

| Light Status | Meaning |
| --- | --- |
| Off | not charging |
| yellow | 0%~80% |
| green | 80%~100% |

## Special Keys

- suspension
    - suspend: `Fn+4`
    - wake up: `Fn`

## Touch Pad

The touch pad can handle all operations of a traditional mouse.
- move
    - move the cursor: move one finger on the pad.
    - scroll the view: move two fingers on the pad. 
- click
    - left click
        - press the primary zone
        - click the pad with one finger.
    - right click
        - press the secondary zone at down-right conner.
        - click the pad with two fingers.