# BlockSite

## What

A productivity app to block unwanted sites and apps.

## Purposes

- efficiency
    - avoid distractions
- security
    - avoid adult contents

## When

- working time to improve productivity
- leisure time to avoid sleeping too late

## Where

- apps
    - android
    - ios
    - windows
- browser extensions
  
## How

- app top
    - attributes
        - on/off
            - toggle
        - password protection
        - site redirection
        - account
    - functionalities
        - regular
            - schedule management
                - group manager
                    - groups
                        - add
                        - delete
                - a group: item manager
                    - attributes
                        - schedule
                            - days
                            - time intervals
                        - on/off
                            - toggle
                        - active
                        - outer look
                            - name
                            - icon
                            - color
                    - items
                        - add
                        - delete
                - item
                    - types
                        - site
                        - app
                        - keyword
            - app limit management
                - for each app installed, there is a daily usage limit.
        - one-time
            - focus mode

### Dependencies

- Android Accessibility

    BlockSite requires this permission to read the content of the screen.

- No battery optimization

    To make BlockSite always on, its battery optimization in android should be turned off to prevent the battery manager from closing the app.